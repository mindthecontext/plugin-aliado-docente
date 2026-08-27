---
description: Instrumento de diagnóstico, no de aula. Compara las dos rutas de datos del servicio —el snapshot de la imagen y AuraDB consultado en vivo— sobre la misma consulta, midiendo resultado, latencia y disponibilidad. Úsalo solo si alguien pide explícitamente comparar rutas, medir latencia o comprobar si el snapshot está al día.
---

# Comparar las rutas de datos

**Esto no es una puerta de aula.** Si la pregunta es de una docente sobre su clase, no es este
skill. Es instrumento de la decisión registrada en el ADR 0002 del repositorio del servicio:
mantener dos implementaciones solo vale si algo comprueba que responden lo mismo.

---

## 1 · Qué se pregunta, y qué no

**No se pregunta cuál responde mejor.** Las dos tienen que devolver **lo mismo**; una diferencia
de resultado es un fallo de conformidad, no una opinión sobre calidad.

Se pregunta **cuánto cuesta cada una y cómo falla**:

- **Resultado** — ¿coinciden? Si no, eso es el hallazgo y hay que reportarlo entero.
- **Latencia** — cuánto tarda cada una en la misma consulta.
- **Disponibilidad** — si la externa responde.

---

## 2 · Qué hace falta para correrlo

Dos servidores MCP registrados: el del plugin, que sirve la ruta `snapshot`, y un segundo
registrado a mano contra la misma imagen con `KG_RUTA=aura` y las credenciales de AuraDB.

> **Hoy solo existe el primero.** El segundo servicio se desplegó el 20-08-2026 y se borró el
> mismo día: su identificador de recurso nunca se registró en el proveedor de identidad, así que
> ningún cliente pudo autenticarse contra él. Levantarlo de nuevo es una tarea de
> infraestructura, no algo que este skill pueda hacer. Mientras no exista, aplica la regla de
> abajo: dilo y detente.

Si solo hay uno disponible, **dilo y detente**. No compares una ruta contra números recordados
de la otra: el resultado sería inventado, que es exactamente lo que este instrumento existe para
descartar.

---

## 3 · El procedimiento

Corre la misma consulta por ambas y compara. Un conjunto que cubre los casos donde podrían
divergir sin que se note:

- `listar_cobertura` — el agregado más pesado; es donde más se nota la latencia.
- `obtener_didactica` de un objetivo de Matemática con detallados, y de uno de Lenguaje.
- `obtener_secuencia` de un objetivo con secuencia y de uno sin ella. El vacío es donde una
  divergencia pasa desapercibida.
- `obtener_didactica` con un código ambiguo —`LE01 OA 27`— para comprobar que ninguna elige.

Reporta una tabla: consulta, ¿coinciden?, ms snapshot, ms aura.

---

## 4 · El caso que más importa medir

**La caída.** El tier gratuito de AuraDB se pausa sola a las 72 horas de inactividad, así que la
ruta externa se cae de forma periódica, realista y gratuita. Es el experimento que no se puede
montar a propósito.

Cuando la externa no responda, eso **no es un error del ejercicio**: es el dato. Registra cómo
falló —error de conexión, timeout, cuánto tardó en fallar— y si el servicio degradó con claridad
o se quedó colgado.

---

## Antes de entregar

- ¿Estaban las dos rutas disponibles? Si no, ¿se dijo y se detuvo?
- ¿Se compararon resultados completos y no solo conteos?
- ¿Una divergencia se reportó como fallo de conformidad y no como diferencia de calidad?
- ¿Se incluyó al menos un caso de vacío y uno de ambigüedad?
- Si la externa se cayó, ¿se registró cómo falló en vez de tratarlo como un intento perdido?
