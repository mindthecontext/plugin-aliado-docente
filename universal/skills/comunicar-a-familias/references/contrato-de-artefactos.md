<!-- Copia generada al derivar el paquete. Editar doctrina/ en la raíz del saber. -->
# Contrato de artefactos

Cuándo la respuesta deja de ser una respuesta y pasa a ser **una cosa que se lleva al aula**.

La diferencia no es de extensión. Una explicación larga sigue siendo conversación; una evidencia
de cierre es un instrumento que se imprime, se reparte y se usa el martes. Este documento fija
cuándo se produce lo segundo, qué forma tiene y qué no puede contener.

---

## 1 · Los cuatro tipos, y la regla de la puerta

| Tipo | Qué es | Forma |
|---|---|---|
| **Evidencia de cierre** | Instrumento breve —1 a 3 preguntas— para comprobar comprensión al final de una clase | Objetivo, preguntas, criterio de éxito, sugerencia de uso |
| **Rúbrica** | Matriz analítica de criterios × niveles | Tabla con cuatro niveles: Inicial · En desarrollo · Logrado · Destacado |
| **Plan de clase** | Inicio, desarrollo y cierre con tiempos | Objetivos trabajados, actividades, evaluación formativa |
| **Guía para estudiantes** | Material que recibe **el estudiante**, no la docente | Instrucciones claras, actividades secuenciadas, espacios de respuesta |

> **La regla de la puerta: si lo que se pide no es uno de estos cuatro, no se produce artefacto.**
> Se responde en la conversación. Un artefacto de tipo inventado no es un artefacto: es una
> respuesta larga con nombre de archivo, y el docente descubre la diferencia cuando intenta usarlo.

**En el título va «Evidencia de cierre», no «ticket de salida».** El primero es el término del
Decreto 67/2018; el segundo es jerga profesional prestada del inglés. Si la docente lo pide con
el segundo nombre se entiende perfectamente y se produce igual — lo que no se hace es devolverle
la jerga: el archivo se llama como lo llama la norma.

---

## 2 · El artefacto es un archivo, no un bloque de texto

Aquí está la diferencia con responder bien. Un instrumento que vive dentro del hilo de una
conversación hay que rescatarlo copiando y pegando, y se pierde en cuanto la conversación sigue.

**Se escribe un archivo**, en la carpeta de trabajo salvo que la docente diga otra cosa, con
nombre descriptivo que incluya nivel y tema:

```
evidencia-cierre-4B-fracciones-equivalentes.md
rubrica-6B-comprension-lectora.md
```

### El formato lo decide quién lo usa, no la comodidad de escribirlo

| Artefacto | Qué le pasa después | Formato |
|---|---|---|
| **Guía para estudiantes**, **rúbrica** | Va **al papel**, tal cual | **HTML con `@media print`** |
| **Plan de clase**, **evidencia de cierre** | La docente lo **adapta** antes de usarlo | **Markdown** |

**Por qué no todo markdown.** Una guía impresa desde markdown sale con márgenes de navegador,
sin control de saltos de página, y con espacios de respuesta que no tienen el alto de un renglón
escrito a mano. Es legible y **no parece material**: parece la impresión de una página web, y
una docente que la reparte lo nota antes que nadie.

Un HTML con hoja de impresión resuelve las tres cosas: `@page { size: A4; margin: 14mm }`,
`break-inside: avoid` en cada bloque que no debe partirse, y cajas de respuesta dimensionadas
para un lápiz. Una rúbrica de cuatro criterios × cuatro niveles pide además `A4 landscape` y
`display: table-header-group`, para que la cabecera se repita si cae en dos páginas.

**Y por qué no todo HTML.** Lo que la docente va a editar tiene que poder editarlo. Un plan de
clase en HTML se lee bien y se retoca mal, y el plan es justamente la pieza que cada persona
ajusta a su curso, su horario y su material.

**En los dos casos, autocontenido**: nada de hojas de estilo externas, tipografías remotas ni
scripts. Se abre en cualquier máquina, sin red, dentro de cinco años.

---

## 3 · La respuesta no repite el artefacto

Cuando el artefacto existe como archivo, **volcarlo entero en la conversación lo duplica y obliga
a leerlo dos veces**. La respuesta hace otra cosa:

1. Dice que está y dónde: *«Te dejé la evidencia de cierre en
   `evidencia-cierre-4B-fracciones-equivalentes.md`»*.
2. Dice **en qué se apoya** — que es lo que el artefacto no puede llevar dentro.
3. Dice qué decisiones se tomaron al armarlo y qué queda al criterio de la docente.

Un resumen de tres líneas de lo que contiene está bien. La transcripción completa, no.

---

## 4 · El respaldo va fuera del artefacto

Un artefacto se usa en aula. Una guía para estudiantes con citas del Decreto 83 al pie no sirve
para nadie: el estudiante no la necesita y a la docente le estorba.

**Dentro del artefacto** va lo que se usa: el objetivo, las preguntas, los criterios, los tiempos.
**En la conversación** van las fuentes con sus tres ejes —autoridad, año, jurisdicción— y el
«cómo llegué» de la regla 7. Ese reparto es el mismo principio que separa el hallazgo de su
evidencia: el instrumento apunta a su respaldo, no lo carga encima.

Excepción única: el **plan de clase** puede citar el código del objetivo oficial —`MA04 OA 08`—
porque ahí la trazabilidad la usa la docente para justificar ante UTP, y le ahorra buscarlo.

---

## 5 · Lo que un artefacto no hace

**No califica.** Una rúbrica propone criterios observables y niveles de desempeño. No fija notas,
no reparte porcentajes y no traduce niveles a calificación. La calificación es decisión de la
docente y de su reglamento de evaluación, y este servicio no lo conoce.

**No inventa objetivos ni códigos.** Si el objetivo no está en la base, no se produce artefacto
sobre él. Se dice que no está.

**No sale de la cobertura.** Nada de Historia, Ciencias, Educación Física, Artes, Música,
Tecnología, media técnico-profesional ni parvularia — tampoco «adaptando» uno de Matemática o
Lenguaje. La adaptación silenciosa de un material a una asignatura que la base no cubre es
exactamente el fallo que la doctrina de respuesta persigue, con un archivo encima que le da
apariencia de rigor.

**No nombra estudiantes reales.** Si la docente los mencionó, en el artefacto van como
«estudiante A», «estudiante B» o por perfil.

---

## 6 · Nunca digas que lo creaste si no lo creaste

**Esta regla se paga con la confianza del producto, y ya se pagó una vez.** En la mesa de trabajo
del prototipo, el agente afirmaba haber guardado una nota en el perfil sin haber llamado a la
herramienta (`MESA-FIX-NOTA-NO-GUARDADA`). El system prompt de aquel sistema lleva desde entonces
una regla crítica sobre acciones.

Aquí el fallo es peor. En la mesa había un panel donde la nota no aparecía y delataba el
problema en segundos. Aquí no hay panel: si la respuesta dice *«te dejé el archivo»* y el archivo
no se escribió, nadie se entera hasta que la docente lo busca para la clase del martes.

> **O se escribe el archivo, o no se afirma que existe.** Nunca «te dejé», «generé» o «guardé»
> sin la escritura real hecha en este mismo turno. Si la escritura falla, se dice que falló y se
> entrega el contenido en la conversación, que es la degradación honesta.

---

## 7 · Antes de entregar

- ¿Es uno de los cuatro tipos? Si no, no es artefacto.
- ¿El formato corresponde a quién lo usa? HTML con hoja de impresión si va al papel; markdown si
  la docente lo va a editar.
- ¿El archivo existe de verdad, escrito en este turno?
- ¿El nombre dice nivel y tema?
- ¿El contenido se sostiene sin la conversación alrededor?
- ¿Las fuentes quedaron **fuera** del artefacto y **dentro** de la respuesta?
- ¿Hay algún nombre real de estudiante que anonimizar?
