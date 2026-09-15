---
name: empezar-aqui
description: Orienta a una docente que no sabe qué pedirle a Aliado Docente — «¿qué asignaturas y niveles cubre?», «¿en qué me puede ayudar con mis clases?», «¿qué le puedo preguntar sobre currículum?», «¿por dónde empiezo con esto?», «¿qué sabes de los objetivos de aprendizaje?». Presenta lo que responde en el idioma de la docente, con la cobertura consultada en vivo y la frontera dicha desde el principio. NO es la puerta para «¿qué puedes hacer?» a secas, que es una pregunta sobre el asistente y no sobre este dominio.
---

# Empezar aquí

Una docente instaló esto y no sabe qué pedirle. Esta puerta la orienta en una pantalla.

> **No es la puerta de «¿qué puedes hacer?» a secas.** Esa pregunta es sobre el asistente
> —qué sabe hacer con el repositorio, con los archivos, con la sesión— y responderla con el
> catálogo de un dominio es cambiarle la pregunta a quien la hizo. Esta puerta se abre cuando
> la consulta menciona clases, currículum, objetivos de aprendizaje, o nombra el servicio.

**Antes de responder, llama a `listar_cobertura`.** Usa lo que devuelva. **Nunca escribas de
memoria cuántos objetivos hay ni qué niveles cubre**: la base cambia y una bienvenida que
envejece mal es peor que no tenerla.

> **Si la herramienta no responde, ese es el tema.** Di que el servicio no está conectado en
> esta superficie —un conector se autoriza por cliente, y tenerlo en uno no lo habilita en
> otro—, y no completes la orientación con cifras recordadas. Una bienvenida que inventa su
> propia cobertura es peor que una que pide conectar.

---

## 1 · Qué decir primero

Una frase de qué es esto, y enseguida el alcance. El alcance no es letra chica: es lo primero
que una docente necesita para saber si le sirve.

> Esto trae conocimiento didáctico del currículum chileno: no qué hay que enseñar —eso está en
> las Bases— sino **qué hay que saber para enseñarlo**. Qué deben dominar antes, dónde se
> atascan, cómo te das cuenta en clase y con qué lo remedias.

Después las cifras que devolvió la herramienta: asignaturas, niveles, total de objetivos.

---

## 2 · Qué puede preguntar, en su idioma

Preséntalo como preguntas, **no como nombres de skills**. A una profesora no le sirve saber que
existe algo llamado `ordenar-la-progresion`; le sirve saber que puede preguntar qué va antes.

- Voy a enseñar fracciones equivalentes en 5°. ¿Qué necesito tener en cuenta?
- Se me atascan en la resta con reserva. ¿Por qué pasa y cómo lo trabajo?
- Tengo un estudiante con TEA en el curso. ¿Cómo adapto sin bajarle la expectativa?
- ¿Cómo sé si entendieron, más allá de la prueba?
- ¿Qué va antes de esto? Estoy armando la unidad.
- ¿Qué dice el Decreto 67 sobre calificar la retroalimentación?

Elige tres o cuatro según lo que la persona haya dicho, y **nómbralas con un contenido
concreto**. «¿Qué necesito para enseñar fracciones en 5°?» invita a probar; «puedes preguntar
por un objetivo» no.

**Qué cambió y en qué versión corre** → `ver_cambios()`. Antes de su línea base no hay registro: dilo así.

---

## 3 · Qué no responde, dicho al principio

Ahorra la decepción de la tercera pregunta.

- **Solo Matemática y Lenguaje**, de 1° básico a 2° medio. No hay Historia, Ciencias, Educación
  Física, Artes, Inglés, ni párvulo, ni técnico-profesional, ni 3° y 4° medio.
- **No diagnostica estudiantes.** Puede decir qué apoyos existen para un perfil que la docente
  aporte; nunca decir qué tiene un niño.
- **No escribe la clase por ti.** Entrega el criterio y la evidencia; el material lo redactas
  con eso a la vista.
- **No recuerda.** No guarda nada de tu curso ni de tus estudiantes entre conversaciones.

Y una advertencia que conviene dar de entrada, porque cambia cómo se lee todo lo demás:
**buena parte de este conocimiento fue inferido por un modelo, no extraído de documentación
oficial.** El servicio lo declara en cada respuesta. Es útil y es una hipótesis.

---

## 4 · Cierra ofreciendo la primera pregunta

Una bienvenida que termina en «pregúntame lo que quieras» no ayuda. Termina proponiendo **una**
pregunta concreta y quédate esperando.

Si la persona ya nombró un curso o un contenido, propón el suyo. Si no, propón uno de
Matemática de enseñanza básica, que es donde la base está más poblada.

---

## Antes de entregar

- ¿La cobertura salió de `listar_cobertura` y no de la memoria?
- Si la herramienta no respondía, ¿se dijo que falta conectar y no se completó con cifras recordadas?
- ¿Se habló en preguntas y no en nombres de skills?
- ¿Se dijo qué **no** responde, incluida la advertencia sobre el conocimiento inferido?
- ¿Termina con una pregunta concreta y no con una invitación vaga?
- ¿Cabe en una pantalla? Una orientación larga se salta entera.
