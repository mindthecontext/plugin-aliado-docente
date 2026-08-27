---
name: preparar-una-clase
description: Prepara la enseñanza de un objetivo concreto — «voy a enseñar fracciones la próxima semana», «me toca pasar la resta con reserva», «cómo armo la clase de X», «qué necesito para enseñar Y en 4°». Entrega qué deben dominar antes, dónde se va a atascar el curso y cómo detectarlo, con qué remediarlo y cómo cerrar sabiendo si resultó.
---

# Preparar una clase

La puerta central. Alguien va a enseñar algo concreto y quiere llegar preparada.

**Lee `references/doctrina-de-respuesta.md` y `references/lo-que-la-base-sostiene.md` antes de
redactar.** Lo segundo importa especialmente aquí: la forma de los datos cambia entre Matemática
y Lenguaje, y leerla mal produce una respuesta que parece completa y no lo está.

Esta puerta es la actividad docente `planificar_ensenanza`. Si el trabajo pasa de una
respuesta, **`references/unidad-de-trabajo.md`** dice cómo se sostiene: se abre expediente, se
lee antes de responder y se anota lo decidido y lo descartado. Una unidad recorre varias
actividades —cambiar de puerta no empieza otro trabajo, sigue el mismo—.

Si la preparación termina en un plan de clase, **`references/contrato-de-artefactos.md` manda
sobre su forma** — incluida la excepción que le permite llevar el código del objetivo dentro,
porque ahí la trazabilidad la usa la docente ante UTP. Y la regla 6 no admite matices: el
archivo se escribe de verdad o no se afirma que existe.

---

## 1 · La primera llamada es `preparar_respuesta_docente`, sin excepción

Si la docente dio un código —`MA05 OA 07`, `LE04 OA 01`— ve directo a `obtener_didactica`: el
código ya fija el curso y no hay nada que buscar.

**En cualquier otro caso** —un contenido y un curso, que es lo habitual— la primera llamada es
`preparar_respuesta_docente` con `tema`, `nivel` y `asignatura`. No `buscar_objetivos`.

`tema` son las palabras del contenido, no la frase entera: `"fracciones equivalentes"`, no
`"me toca pasar fracciones la otra semana"`.

Devuelve de una vez los candidatos del nivel pedido **y de los dos vecinos**, con la didáctica y
la secuencia de cada uno. Eso hace innecesario el paso 2 para los objetivos que ya trae.

### Lo que hay que mirar primero en la respuesta

**`advertencia_de_nivel`.** Si no viene `null`, léela antes que nada y **trasládala a la
docente**. Significa que la expresión que ella usó no existe en el nivel que nombró y sí en otro.
Ella puede tener razones —adelantar material, otra progresión del colegio— pero la decisión es
suya y necesita el dato. Di cuál de los dos objetivos estás desarrollando y por qué, **antes** de
entregar nada.

> Esto existe por un caso real. Una docente preguntó por «fracciones equivalentes» en 4°. Esa
> frase aparece, literal, en **un solo objetivo de los 619 del currículum**: MA05 OA 07, de 5°.
> Cuarto sí tiene fracciones —MA04 OA 08, 09 y 10—, pero ninguno se llama así. Responder sobre
> uno de ellos sin decirlo es acertar de lado y sonar seguro.

**`candidatos`.** Si hay varios en el nivel pedido y ninguno domina, muestra código y texto
oficial y pregunta. Desarrollar el objetivo equivocado con todo el detalle es peor que preguntar.

**`busqueda.truncado`.** Si no es `null`, hubo más coincidencias de las que trajo. Dilo o vuelve
a llamar con `maximo_objetivos` más alto.

**Si `candidatos` viene vacío**, dilo y detente: *«no encuentro ese objetivo en el currículum
estructurado»*. Puede que el contenido se llame de otro modo —pregúntale a la docente cómo lo
nombra el texto que usa—. **No lo completes con lo que sabes del currículum chileno.** Esa es la
cicatriz que originó toda la doctrina de este servicio.

**Si devuelve una ambigüedad de código**, con varios candidatos de cursos distintos, no elijas
tú. Pregunta de qué curso habla.

---

## 2 · Pide la didáctica y léela con su forma

La didáctica del objetivo elegido **ya viene** en el `expediente` del paso 1: no la vuelvas a
pedir. `obtener_didactica` solo hace falta si la docente dio el código directamente, o si
desarrollas un objetivo que no estaba entre los candidatos.

Lo que sí falta siempre es `obtener_criterio` con ámbito `planificacion` —o
`didactica_matematica` / `didactica_lenguaje` si la pregunta es de una de las dos—. Viene listado
en `pendiente` justamente porque no puede venir incluido: cada pack pesa entre 11 y 18 mil
caracteres.

> **En Matemática, los errores llegan con `causa` y `deteccion` nulas.** No están vacíos: el
> porqué y el ejemplo cuelgan de `detallados`. Si lees solo los campos del error, dirás que la
> base no explica lo que sí explica.
>
> **En Lenguaje es al revés**: los campos están llenos y no hay detallados. Pero los errores de
> Lenguaje son genéricos del eje —48 nombres distintos repartidos entre 696 errores—, así que se
> presentan por lo que son.

---

## 3 · El orden de la respuesta, que no es negociable

**Los errores anticipados van antes de las actividades, no como advertencia al final.** Es la
diferencia entre preparar una clase y decorarla.

1. **Qué deben traer.** Los conocimientos previos, con su `nivel_dificultad` cuando lo traigan.
   Si el bloque llegó vacío, dilo: la base no lo declara para ese objetivo.
2. **Dónde se va a atascar el curso y cómo lo vas a notar.** Cada error con su porqué y con la
   señal concreta en el cuaderno o en la conversación. Esto es el núcleo.
3. **Con qué lo remedias.** Las remediaciones asociadas a cada error, no en una lista suelta.
4. **En qué contexto tiene sentido** y qué conceptos introduce.
5. **Cómo cierras sabiendo si resultó.** Los indicadores, cruzados con los errores del punto 2.

---

## 4 · Nunca entregues la clase como si fuera la única posible

Entrega criterio para armarla. Una secuencia minuto a minuto presentada como *la* clase de
fracciones convierte conocimiento didáctico en una receta, y la docente sabe cosas de su curso
que el servicio no sabe.

Si pide explícitamente una guía o un material, esa es otra puerta: `armar-un-material`.

---

## 5 · Declara la procedencia sin volverla el tema

No conviertas la respuesta en un tratado sobre calidad de datos, pero tampoco presentes
inferencias como hechos.

- Una línea al final: qué salió de documentación oficial y qué infirió un modelo.
- Si el objetivo es de **Lenguaje**, di además que no consta el origen de esos nodos —vienen con
  `estado: desconocido`—, que es distinto de saber que fueron inferidos.
- Si `cobertura` trae `nota`, esa nota va en la respuesta.

---

## Antes de entregar

- ¿La primera llamada fue `preparar_respuesta_docente`, salvo que la docente diera el código?
- Si vino `advertencia_de_nivel`, ¿se le trasladó a la docente antes del material?
- ¿Se cerró con «Decisiones que tomé yo, y conviene que revises»?
- ¿Se declaró en una línea lo que no se consultó, tomándolo de `no_pertinente`?
- ¿Se confirmó cuál es el objetivo antes de desarrollarlo?
- Si la búsqueda no devolvió nada, ¿se dijo y se detuvo, sin completar de memoria?
- En Matemática, ¿se entró a `detallados` para el porqué y el ejemplo?
- ¿Los errores anticipados van **antes** de las actividades?
- ¿Cada remediación está pegada al error que remedia?
- ¿Los bloques vacíos se declararon como «la base no lo tiene», nunca como «no existe»?
- ¿Se distinguió lo extraído de lo inferido, y en Lenguaje lo de origen desconocido?
- ¿Se entregó criterio y no una clase cerrada?
