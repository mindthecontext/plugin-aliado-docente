<!-- Copia generada al derivar el paquete. Editar doctrina/ en la raíz del saber. -->
# Lo que esta base sostiene, y lo que no

Medido sobre el grafo, no sobre su documentación. Léelo antes de concluir que algo «no existe»:
buena parte de lo que parece un hueco es una diferencia de forma, y buena parte de lo que parece
completo es una plantilla.

---

## Las dos asignaturas guardan la didáctica de manera distinta

Ninguna de las dos está incompleta, y **comparar campo contra campo lleva a conclusiones
falsas.**

| | Matemática | Lenguaje |
|---|---|---|
| Errores comunes | 405 | 696 |
| Explican por qué ocurre | 370 (91%) | 696 (100%) |
| Dicen cómo notarlo en clase | **405 (100%)** | 652 (94%) |
| Dónde está esa explicación | en un `ErrorDetallado` que cuelga del error | en los campos `causa` y `deteccion` |

En **Matemática**, `causa` y `deteccion` vienen nulas y el conocimiento está un salto más abajo:
los 405 errores tienen `ErrorDetallado`, con `descripcion` —el porqué— y `ejemplo` —cómo se ve
en el cuaderno—. Al leer un error de Matemática hay que entrar en `detallados`, o parecerá que
falta lo que sí está.

En **Lenguaje** es al revés: los campos están llenos y no hay ningún detallado.

---

## Pero la calidad sí es asimétrica, y va en el sentido contrario al que sugiere el conteo

| | Matemática | Lenguaje |
|---|---|---|
| Errores con nombre distinto | **360 de 360** | **48 de 696** |
| Errores por objetivo | 1, 2 o 3 | exactamente 2, en los 348 |
| Contextos por objetivo | 1 o 2 | exactamente 2, en los 348 |
| Conceptos por objetivo | de 1 a 4 | exactamente 1, en los 348 |
| Secuencia declarada | 228 y 228 relaciones | **0 y 0** |
| Bloques y unidades | 224 y 263 | **0 y 0** |
| Estrategias de apoyo CEA | 1.952 | **0** |
| Procedencia de los objetivos | `extraido` | `desconocido` |

En Lenguaje, un mismo error —«Cambios de tiempo verbal o de persona narrativa sin control»—
aparece en **47 objetivos distintos**. Es una plantilla por eje, no didáctica de ese objetivo.
En Matemática no se repite ninguno.

**Consecuencias que hay que decirle a la docente cuando corresponda:**

- **`obtener_secuencia` devuelve vacío para los 350 objetivos de Lenguaje.** No el 22-36%: el
  100%. Ese rango es de Matemática. En Lenguaje la alternativa son los conocimientos previos.
- **`obtener_adaptaciones` no trae estrategias CEA en Lenguaje.** Ninguna. Sí trae adecuaciones.
- **Los errores de Lenguaje son genéricos del eje.** Pueden servir y hay que presentarlos por lo
  que son: no salieron de analizar ese objetivo.
- **Los objetivos actitudinales de Lenguaje traen errores comunes**, y los comparten entre sí.
  En Matemática, correctamente, no traen ninguno.

---

## El código MINEDUC no identifica al objetivo

**179 de los 350 objetivos de Lenguaje declaran un `codigo_mineduc` que no corresponde a su
nivel**: los 112 de 4°, 5° y 6° básico están codificados `LE01`, de primero. En Matemática son
18, los de segundo medio, con formato `MA22` en vez de `MA2M`.

Las herramientas ya lo resuelven: preguntan primero por el `uid` —uniforme y fiable en los 619—
y solo después por el código declarado. Lo que hay que saber al leer una respuesta:

- El `codigo_mineduc` que devuelve un objetivo **puede no ser el de su curso**. Al nombrarlo
  para la docente, usa el nivel que dice el `uid`, no el código.
- Cinco códigos siguen sin resolución única —`LE01 OA 27` a `30` y `LE01 OA G`—. Ahí la
  herramienta devuelve los candidatos y **no elige**. Pregunta a la docente de qué curso habla;
  no escojas tú.

---

## La cobertura, por herramienta

| Herramienta | Qué tan poblada está |
|---|---|
| `obtener_didactica` | indicadores 100% · errores, remediaciones y contextos 90% · previos 87% · detallados 34% |
| `obtener_adaptaciones` | adecuaciones 100% · CEA 39% (nada en Lenguaje) · adaptados 34% |
| `obtener_secuencia` | 22-36% en Matemática · **0% en Lenguaje**. Cada vínculo trae tipo (esencial/facilitador), justificación y procedencia propia: 71 validados a mano, 203 extraídos |
| `buscar_objetivos` | nivel 100% · eje 79% (los 133 actitudinales no tienen eje) |
| `listar_cobertura` | estructural, siempre disponible |
| `obtener_criterio` | 8 ámbitos curados a mano, no generados |
| `fundamentar` | 1167 fragmentos de 37 fuentes, 1984-2025 |

**Filtrar por eje excluye los actitudinales**, y es correcto: no pertenecen a ninguno. Pero una
búsqueda sin filtro debe incluirlos.

---

## Lo que no está en el corpus de fundamentación

El grueso de las 37 fuentes es normativa y orientación del MINEDUC, más evidencia internacional
—OECD, EEF, DfE, UNESCO, CAST—.

> **Ojo si conoces la versión anterior de este documento.** Hasta el 21-08-2026 aquí decía que
> **no había ninguna fuente de didáctica chilena no ministerial**, y era cierto. Dejó de serlo:
> entraron los tres títulos de Mabel Condemarín —lectura silenciosa sostenida, integración de
> modelos de lectura y escritura, y «Dame la mano»— como `referencia_profesional`, y con ellos
> el corpus llega hasta 1984. Si al preguntar por lectura inicial descartas esa clase de fuente
> porque «no hay», estarás ocultando justo lo que se fue a buscar.

Un solo nivel de autoridad queda declarado y vacío: `investigacion_academica`. Pedirlo y recibir
cero **no significa «no hay nada relevante»**: significa que el corpus no tiene fuentes de esa
clase. La herramienta lo dice; hay que trasladarlo.

---

## El mapa curricular organiza; no excluye

Las Bases Curriculares entraron completas al corpus, y 72 de sus 122 fragmentos —Artes,
Ciencias, Ed. Física, Historia, Tecnología, Inglés, Música y Orientación— llevan la marca
`fuera_de_mapa`. **Se sirven con normalidad**: son información válida y citable.

Lo que la marca gobierna es la frontera, y `fundamentar` la declara en `advertencias` cuando
cita alguno: para esas asignaturas **no hay grafo, ni objetivos de aprendizaje, ni
didáctica**. Puedes citar qué dicen las Bases de Historia; **no puedes** armar una
planificación, una secuencia ni una evaluación sobre objetivos de Historia, porque el eje
organizador de esas actividades es el KG curricular y el KG solo tiene Matemática y Lenguaje.

La distinción operativa: *informar* sobre una asignatura no cubierta, sí, con su cita;
*organizar enseñanza* sobre ella, no — y se dice por qué, ofreciendo lo que sí: las
actividades completas sobre Matemática y Lenguaje.

## La audiencia también tiene límite

Parte del corpus habla al nivel de gestión escolar o de política —TALIS, planes de mejora,
cultura evaluativa institucional— y no al de aula. No hay etiqueta mecánica que lo separe.
La regla: **cuando la pregunta es institucional** («queremos definir una postura de colegio»,
«cómo cambio la cultura evaluativa del establecimiento»), se responde con las fuentes y se
declara que este servicio acompaña la decisión pedagógica de aula; la política institucional
corresponde al equipo directivo. Igual que hace `ia-en-el-aula`.

## Fuera de cobertura, sin excepciones

Dos asignaturas —Matemática y Lenguaje— y diez niveles: 1° a 8° básico, 1° y 2° medio.

**No hay** Historia, Ciencias, Educación Física, Artes, Tecnología, Inglés, ni orientación; ni
educación parvularia; ni media técnico-profesional; ni 3° y 4° medio.

Y no hay estudiantes: el servicio no guarda ni recuerda nada de ningún niño.
