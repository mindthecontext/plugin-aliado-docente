---
description: Prepara el criterio y la evidencia para redactar una guía, una rúbrica o un set de ejercicios — «hazme una guía de fracciones para 5°», «necesito una rúbrica», «arma ejercicios de esto», «prepárame material para la clase». El servicio no genera el material: entrega con qué redactarlo para que ataque los errores reales del objetivo.
---

# Armar un material

«Hazme una guía.» El material lo redactas tú con lo que este servicio entrega — igual que en
Feedback Formativo, donde el workflow es del servicio y el texto es del modelo.

**Lee `references/doctrina-de-respuesta.md` y `references/lo-que-la-base-sostiene.md`.**

Esta puerta es la actividad docente `crear_recurso`. Si el trabajo pasa de una respuesta,
**`references/unidad-de-trabajo.md`** dice cómo se sostiene: se abre expediente, se lee antes
de responder y se anota lo decidido y lo descartado. Una unidad recorre varias actividades
—cambiar de puerta no empieza otro trabajo, sigue el mismo—.

Si la respuesta termina en un instrumento para el aula —evidencia de cierre, rúbrica, plan de
clase o guía para estudiantes—, **`references/contrato-de-artefactos.md` manda sobre su
forma**. Es la puerta que más artefactos produce, así que su regla de los cuatro tipos es la
que más va a doler: lo que cae fuera se responde en la conversación y no se disfraza de
archivo. Y la regla 6 no admite matices — el archivo se escribe de verdad o no se afirma que
existe.

---

## 1 · Nunca redactes antes de pedir la didáctica

Es la regla que hace la diferencia entre un material del dominio y un material genérico con
membrete curricular.

> **Un material que no anticipa ningún error del curso es un material genérico.** Los ítems
> tienen que atacar los errores que la base declara para ese objetivo, no ejercicios plausibles
> del tema.

Antes de escribir una sola línea, `preparar_respuesta_docente` con `tema`, `nivel` y
`asignatura`. Trae la didáctica y la secuencia de los candidatos del nivel pedido y de los dos
vecinos, y es lo que impide redactar una guía impecable sobre el objetivo equivocado.

**Si viene `advertencia_de_nivel`, resuélvela con la docente antes de redactar.** Un material ya
maquetado sobre el objetivo de otro curso es trabajo perdido para las dos partes, y cuesta más
retirarlo que no haberlo hecho.

Solo si la docente dio el código directamente se va a `obtener_didactica` sin pasar por aquí.

Después, siempre, `obtener_criterio` con el ámbito que corresponda —`didactica_matematica`,
`didactica_lenguaje`, `lectura_inicial`, `evaluacion_formativa` si es una rúbrica—. Aparece en
`pendiente` porque no viene incluido: cada pack pesa entre 11 y 18 mil caracteres.

---

## 2 · De dónde sale cada parte del material

| Parte | De dónde |
|---|---|
| Qué se practica | `texto_oficial` del objetivo |
| Qué se supone que ya saben | `conocimientos_previos` |
| **Los distractores y los ítems difíciles** | `errores_comunes` y sus `detallados` |
| Los ejemplos concretos | el `ejemplo` de cada detallado, en Matemática |
| El contexto de los enunciados | `contextos` |
| Los criterios de la rúbrica | `indicadores`, cruzados con los errores |
| Cómo se remedia lo que falle | `remediaciones` |

En Matemática, el `ejemplo` de un detallado suele describir la respuesta equivocada exacta: es
material de distractor casi literal.

---

## 3 · Entrega el material y, aparte, en qué se apoya

Dos bloques separados:

1. **El material**, redactado y listo para usar.
2. **En qué se apoya y qué revisar**: qué error ataca cada ítem, qué salió de documentación
   oficial y qué infirió un modelo, y qué decisiones tomaste tú porque la base no las cubría.

El segundo bloque es lo que permite a la docente corregirlo con su criterio. Sin él, el material
se usa como si estuviera validado.

---

## 4 · Lo que no se hace

**No se entrega material de asignaturas no cubiertas**, ni «adaptando» uno de Matemática. Si
pide una guía de Ciencias, se declara el límite y se detiene — y no se ilustra el principio con
un ejemplo del área excluida, que es la regla 5 de la doctrina.

**No se inventan objetivos ni códigos.** Si el objetivo no está en la base, se dice.

**No se califica.** Una rúbrica propone criterios observables; no fija notas ni ponderaciones.

---

## Antes de entregar

- ¿La primera llamada fue `preparar_respuesta_docente`, salvo que la docente diera el código?
- Si vino `advertencia_de_nivel`, ¿se resolvió con la docente **antes** de redactar?
- ¿Se tuvo la didáctica **antes** de redactar?
- ¿Se cerró con «Decisiones que tomé yo, y conviene que revises»?
- ¿Se declaró en una línea lo que no se consultó, tomándolo de `no_pertinente`?
- ¿Cada ítem difícil ataca un error declarado, y se dice cuál?
- ¿El material y su fundamento van en bloques separados?
- ¿Se dijo qué decisiones son tuyas por falta de datos?
- ¿Se distinguió lo extraído de lo inferido?
- Si el objetivo estaba fuera de cobertura, ¿se declaró el límite sin cruzarlo con ejemplos?
