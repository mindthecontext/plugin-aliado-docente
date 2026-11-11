---
name: fundamentar-una-decision
description: Busca el respaldo normativo o de evidencia de una decisión pedagógica — «¿qué dice el Decreto 67 sobre esto?», «con qué respaldo defiendo esta adecuación», «¿es obligatorio?», «qué dice la normativa de evaluación», «necesito citar algo para el consejo de profesores». Devuelve cada fuente con su nivel de autoridad, su jurisdicción y su año, sin colapsarlos en un ranking.
---

# Fundamentar una decisión

Alguien necesita respaldo citable: para defender una adecuación, para una reunión de
departamento, o simplemente para saber si algo es obligatorio o recomendable.

**Lee `references/doctrina-de-respuesta.md` y `references/lo-que-la-base-sostiene.md`.**

Esta puerta es la actividad docente `justificar_decision`. Si el trabajo pasa de una respuesta,
**`references/unidad-de-trabajo.md`** dice cómo se sostiene: se abre expediente, se lee antes
de responder y se anota lo decidido y lo descartado. Una unidad recorre varias actividades
—cambiar de puerta no empieza otro trabajo, sigue el mismo—.

---

## 0 · Parte por el pack normativo, y verifica con la herramienta

**Lee `references/pack-normativo.md` antes de buscar.** Es la síntesis revisada del respaldo
normativo de esta puerta: cada afirmación lleva punteros a los fragmentos que la sostienen, y
una sección de lo que la base NO respalda — que es tan importante como el resto.

El flujo que ganó el lab (21-08-2026, juicio ciego y eje mecánico):

1. Si la pregunta cae en el pack, responde desde él **y verifica los punteros que vayas a
   citar** llamando a `fundamentar` con los términos técnicos de esa afirmación. La regla de
   conflicto está en la cabecera del pack: si contradice al fragmento, **manda el fragmento**.
2. Si la pregunta no cae en el pack —o cae en su sección de «no respaldado»— usa `fundamentar`
   directamente, o declara el límite tal como el pack lo declara.
3. Nunca cites el pack como fuente ante la docente: **la fuente es el fragmento** (decreto,
   ley, orientación, con su año). El pack es el índice, no la autoridad.

## 1 · Llama a `fundamentar` y filtra con criterio

Pasa la pregunta tal como la formuló la docente en `consulta`. Usa `nivel_minimo` solo si pidió
explícitamente normativa —«¿es obligatorio?» sí lo pide; «¿qué se recomienda?» no—.

> **El motor es léxico.** Encuentra bien los términos exactos —«Decreto 67», «DUA», «evaluación
> formativa»— y falla con la paráfrasis. Si no encuentra nada, **reformula con el término
> técnico** antes de concluir que el corpus no lo tiene, y dilo cuando lo hagas.

---

## 2 · Los tres ejes van los tres, siempre

Cada fragmento trae `authority_level`, `jurisdiction` y `year`. **No los colapses en un orden.**

- El **nivel** ordena: normativa obligatoria por encima de orientación oficial, y esta por
  encima de evidencia internacional.
- La **jurisdicción** ordena al revés: lo chileno pesa más que lo internacional para una
  decisión que se toma en Chile.
- El **año** no dice vigencia. Las Bases son de 2012 y rigen; una orientación de 2020 puede
  estar derogada. El corpus no declara vigencia y la herramienta lo reporta como no derivable:
  trasládalo, no lo rellenes.

Quien lee decide cuál pesa más para su pregunta. Esa decisión no es tuya.

---

## 3 · Un encabezado sobre una cita es una afirmación tuya

Si escribes **«El Decreto 67 exige retroalimentación continua»** y debajo citas el artículo, ese
título es una afirmación del servicio que hereda la autoridad del decreto sin haberla ganado.

> Si el encabezado no se sostiene con el texto citado, **cita el artículo sin resumirlo.**

Y usa `cautions` cuando el fragmento lo traiga: son los límites que la curaduría escribió para
ese fragmento en particular, y existen precisamente para que no se sobre-extienda.

---

## 4 · Distingue obligatorio de recomendable, explícitamente

Es lo que la docente vino a buscar, aunque no lo diga así. Sepáralo:

- **Obligatorio** — normativa: decretos, leyes, Bases Curriculares, MBE.
- **Institucionalmente respaldado** — orientaciones del MINEDUC, no vinculantes.
- **Evidencia** — síntesis internacional. Fortalece un argumento; no obliga a nada.

---

## 5 · Cuando el corpus no tiene la clase de fuente que hace falta

Dos niveles están declarados y **vacíos**: `investigacion_academica` y `referencia_profesional`.
Y las 24 fuentes son normativa MINEDUC más evidencia internacional: **no hay didáctica chilena
no ministerial** en el corpus.

Si la pregunta pedía justamente eso, dilo: *«el corpus no tiene fuentes de esa clase»*. No es lo
mismo que «no hay nada relevante», y no se sustituye por lo más parecido que haya.

---

## Antes de entregar

- ¿Cada cita trae nivel, jurisdicción y año?
- ¿Se distinguió lo obligatorio de lo recomendable?
- ¿Ningún encabezado propio afirma más que el texto citado?
- ¿Se trasladaron los `cautions` del fragmento?
- ¿Se dijo que la vigencia no es derivable, en vez de deducirla del año?
- Si no se encontró nada, ¿se reformuló con el término técnico antes de concluir?
- Si faltaba la clase de fuente, ¿se dijo, en vez de ofrecer la más parecida?
