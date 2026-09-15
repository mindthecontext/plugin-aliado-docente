---
description: Ordena el contenido de una unidad y explica qué va antes de qué — «¿qué va primero?», «en qué orden armo la unidad», «por qué el curso no está listo para esto», «qué tienen que saber antes», «cómo secuencio esto». La puerta más delicada: la secuencia declarada existe solo en Matemática, y ahí para un tercio de los objetivos.
---

# Ordenar la progresión

«¿Qué va antes?» Y aquí la base tiene un hueco grande que **hay que decir bien**, porque decirlo
mal produce la peor afirmación que este servicio puede hacer.

**Lee `references/doctrina-de-respuesta.md` y `references/lo-que-la-base-sostiene.md` antes de
responder.**

Esta puerta es la actividad docente `secuenciar_aprendizaje`. Si el trabajo pasa de una
respuesta, **`references/unidad-de-trabajo.md`** dice cómo se sostiene: se abre expediente, se
lee antes de responder y se anota lo decidido y lo descartado. Una unidad recorre varias
actividades —cambiar de puerta no empieza otro trabajo, sigue el mismo—.

---

## 1 · Lo primero: en Lenguaje no hay secuencia

> **`obtener_secuencia` devuelve vacío para los 350 objetivos de Lenguaje.** No un porcentaje:
> los 350. No hay `PRECEDE_A`, no hay `REQUIERE_PREVIO`, no hay bloques ni unidades.
>
> En **Matemática** sí la hay, para un 22-36% de los objetivos según el tipo de enlace.

Así que antes de llamar a la herramienta ya sabes si vas a recibir algo. Y sabes que recibir
vacío **es lo esperable**, no una anomalía.

---

## 2 · Cómo se dice el vacío

Esta es la frase que importa de toda la puerta:

> ✅ «El servicio no tiene secuencia declarada para este objetivo.»
> ❌ «Este objetivo no tiene prerrequisitos.»

La segunda es una afirmación sobre la didáctica del contenido, y es casi siempre falsa: todo
objetivo de matemáticas tiene prerrequisitos. Lo que ocurre es que **nadie los declaró en esta
base**, que es una afirmación sobre la base.

Una docente que lea la segunda va a armar su unidad creyendo que puede partir por ahí.

---

## 3 · Qué ofrecer cuando no hay secuencia, que es casi siempre

**Los conocimientos previos cubren el 87% de los objetivos.** No son lo mismo que una secuencia
—no dicen qué objetivo va antes, dicen qué hay que dominar— pero responden buena parte de la
pregunta real.

Llama a `obtener_didactica` y ofrece:

1. Los `conocimientos_previos` del objetivo, con su `nivel_dificultad`.
2. Los `errores_comunes`, que a menudo apuntan hacia atrás: un error que revela un prerrequisito
   no consolidado es información de secuencia por otra vía.
3. Si la unidad abarca varios objetivos, `buscar_objetivos` por eje y nivel para ver qué hay
   disponible, y ordénalos por lo que dicen sus previos, diciendo que ese orden es tuyo y no de
   la base.

---

## 4 · Cuando sí hay secuencia

**Cada vínculo trae su porqué, y hay que usarlo.** No es solo «este objetivo va antes»:

- **`tipo`** distingue el prerrequisito **esencial** —sin eso el objetivo no se sostiene— del
  **facilitador**, que ayuda. Si falta uno esencial, la respuesta es volver atrás; si falta
  uno facilitador, es apoyar de otra forma. Presentarlos igual borra la decisión.
- **`justificacion`**, cuando existe, dice por qué en palabras de la curaduría: úsala, es
  mejor que cualquier paráfrasis.
- **`procedencia` del vínculo**, distinta de la del objetivo: hay 71 `validado_manual` y 203
  `extraido`. Un vínculo validado a mano puede afirmarse; uno inferido se declara como tal.


En Matemática, `obtener_secuencia` devuelve `objetivo_previo`, `objetivo_siguiente`, el `bloque`
y la `unidad`, con los objetivos vecinos resueltos completos.

Los enlaces **cruzan cursos**: un objetivo de 4° apunta a 3° y a 5°. Eso es lo más valioso de
esta puerta, porque responde «¿por qué mi curso no está listo?» señalando el año anterior.

Presenta la cadena, no los nodos sueltos: qué viene antes, este, qué viene después. Y di de
dónde salió: la procedencia de esos enlaces también viaja.

---

## Antes de entregar

- ¿Se dijo «el servicio no tiene secuencia declarada», nunca «el objetivo no tiene prerrequisitos»?
- Si es Lenguaje, ¿se dijo que la asignatura entera no tiene secuencia, y no se insinuó que fuera de ese objetivo?
- ¿Se ofrecieron los conocimientos previos como lo que sí hay?
- Si se propuso un orden propio, ¿se dijo que es propio y no de la base?
- Si había secuencia, ¿se presentó como cadena y con los cursos que cruza?
- ¿Se declaró la procedencia?
