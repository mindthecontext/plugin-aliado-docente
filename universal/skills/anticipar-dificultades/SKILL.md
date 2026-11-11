---
name: anticipar-dificultades
description: Explica por qué un curso se atasca en algo y cómo se detecta en clase — «se me atascan en fracciones», «están sumando numeradores y denominadores», «no entienden la resta con reserva», «por qué les cuesta tanto esto», «cómo me doy cuenta de que no entendieron». Entra por el error, no por la planificación.
---

# Anticipar dificultades

La docente ya está enseñando y algo no está resultando. No quiere una clase: quiere entender qué
está pasando.

**Lee `references/doctrina-de-respuesta.md` y `references/lo-que-la-base-sostiene.md`.**

Esta puerta es la actividad docente `diagnosticar_brecha`. Si el trabajo pasa de una respuesta,
**`references/unidad-de-trabajo.md`** dice cómo se sostiene: se abre expediente, se lee antes
de responder y se anota lo decidido y lo descartado. Una unidad recorre varias actividades
—cambiar de puerta no empieza otro trabajo, sigue el mismo—.

Es la puerta que más se apoya en la regla 1: buena parte de estos errores son inferidos, y aquí
se está explicando **por qué** falla un niño real. Presentar una hipótesis del sistema como la
causa comprobada es el fallo más caro de esta puerta.

---

## 1 · Localiza el objetivo desde el síntoma

La docente casi nunca da un código. Da una conducta: «suman numeradores y denominadores».

Si no mencionó curso, pregúntalo **antes de buscar**: el mismo síntoma en 3° y en 7° son
objetivos distintos.

Con el curso en mano, la primera llamada es `preparar_respuesta_docente` con `tema`, `nivel` y
`asignatura` — no `buscar_objetivos`. El `tema` es el contenido detrás del síntoma
(«suma de fracciones»), no la conducta literal.

Trae la didáctica de todos los candidatos, así que el paso 2 ya tiene con qué trabajar sin otra
llamada.

**Aquí el nivel vecino importa más que en ninguna otra puerta.** Un curso que se atasca suele
estar tropezando con un objetivo del año anterior, no con el suyo: por eso `nivel_relativo:
anterior` entre los candidatos no es ruido, es la hipótesis más probable. Y si viene
`advertencia_de_nivel`, trasládala.

Confirma cuál es antes de explicar. Si `candidatos` viene vacío, dilo y detente.

---

## 2 · Entra por los errores, no por la planificación

La didáctica ya viene en el `expediente`; entra a ella directo y **empieza por
`errores_comunes`**. Los conocimientos previos vienen
después, como explicación de fondo, no como apertura.

> **En Matemática**, `causa` y `deteccion` vienen nulas y lo que buscas está en `detallados`:
> `descripcion` es el porqué y `ejemplo` es la señal concreta. Entra ahí siempre.
>
> **En Lenguaje**, están en `causa` y `deteccion` del propio error — pero son genéricos del eje.

Busca el error que **coincide con el síntoma que describió**. Si ninguno coincide, dilo: *«la
base no registra ese error para este objetivo»*. No fuerces el más parecido, y no inventes una
explicación plausible.

---

## 3 · Responde en este orden

1. **Qué está pasando**, nombrando el error como lo nombra la base.
2. **Por qué ocurre.** La causa, y aquí la formulación importa: *«el sistema infiere que esto
   ocurre porque…»* cuando el nodo es inferido.
3. **Cómo confirmarlo mañana en clase.** La señal concreta —el ejemplo del detallado, o el campo
   `deteccion`—. Esto es lo que la docente puede usar el lunes.
4. **Qué hacer.** Las remediaciones de ese error, no de la lista completa.
5. **Qué mirar más atrás**, si el error apunta a un prerrequisito: los conocimientos previos.

---

## 4 · Lo que no se hace aquí

**No se diagnostica al niño.** Un error común es un patrón del contenido, no una característica
del estudiante. Si la docente desliza «¿será que tiene discalculia?», reconduce con la
formulación de referencia de la doctrina y ofrece lo que sí se puede.

**No se concluye del vacío.** Si el objetivo no tiene errores declarados —hay objetivos así— eso
no significa que el contenido no tenga dificultades típicas. Significa que la base no las tiene.

---

## Antes de entregar

- ¿La primera llamada fue `preparar_respuesta_docente`, salvo que la docente diera el código?
- Si vino `advertencia_de_nivel`, ¿se le trasladó a la docente antes del material?
- ¿Se cerró con «Decisiones que tomé yo, y conviene que revises»?
- ¿Se declaró en una línea lo que no se consultó, tomándolo de `no_pertinente`?
- ¿Se confirmó el objetivo y el curso antes de explicar?
- En Matemática, ¿se leyeron los `detallados` en vez de dar por vacíos `causa` y `deteccion`?
- ¿El error elegido coincide de verdad con el síntoma, o se forzó el más parecido?
- ¿La causa se presentó como inferencia cuando el nodo es inferido?
- ¿Hay una señal concreta y observable, no solo una explicación?
- ¿Las remediaciones están pegadas a su error?
- ¿Se evitó cualquier afirmación sobre el estudiante?
