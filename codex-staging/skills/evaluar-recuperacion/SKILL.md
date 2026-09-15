---
name: evaluar-recuperacion
description: Instrumento de diagnóstico, no de aula. Mide si `fundamentar` encuentra el fragmento correcto entre los primeros resultados, sobre un conjunto de consultas conocidas. Úsalo solo si alguien pide evaluar la recuperación, medir el buscador o decidir si vale la pena añadir búsqueda semántica.
---

# Evaluar la recuperación

**Esto no es una puerta de aula.** Es el instrumento del lab que decide si la recuperación densa
entra al servicio, registrado en la etapa 3 del contrato.

---

## 1 · La pregunta que decide

Hoy `fundamentar` recupera con **BM25 léxico**: cero megabytes, instantáneo. La alternativa es
añadir un modelo de embeddings multilingüe cuantizado —unos 120 MB en la imagen y uno a tres
segundos de arranque en frío— y combinar ambos.

> **La compuerta:** el denso entra solo si gana lo suficiente para justificar esos 120 MB y ese
> arranque. No basta con que gane.

Y lo que hay que medir es **si el fragmento correcto aparece entre los primeros**, no si la
respuesta final «suena mejor». Lo segundo es imposible de comparar y es donde estos ejercicios
se pierden.

---

## 2 · Dónde falla lo léxico, que es lo que hay que provocar

BM25 es fuerte donde los términos son exactos —«Decreto 67», «DUA», «fracciones equivalentes»—
y su punto ciego es la **paráfrasis**: «cómo hago que entiendan» no encuentra «estrategias de
remediación».

Un conjunto de prueba que solo use términos técnicos no mide nada: lo léxico va a ganar por
construcción. **La mitad de las consultas tienen que estar escritas como habla una docente.**

---

## 3 · El conjunto de referencia

Las nueve conversaciones de la bitácora de validación del prototipo, que ya traen la respuesta
esperada y su evaluación pedagógica. Son consultas reales, no escritas para el ejercicio.

Para cada una: ¿aparece el fragmento que la bitácora considera correcto? ¿En qué posición?

---

## 4 · Cómo se reporta

Una tabla con consulta, posición del fragmento correcto —o «no aparece»— y el nivel de autoridad
de lo que sí salió primero.

Y el resumen honesto: en cuántas de las nueve apareció entre los tres primeros. Si son ocho, el
denso tiene poco que ganar. Si son cuatro, la conversación cambia.

> **Hoy la rama densa no existe en el código.** Este skill mide la léxica sola y establece la
> línea base. Comparar dos ramas exige implementar la segunda primero, y esa decisión depende
> justamente de lo que mida esto.

---

## Antes de entregar

- ¿Al menos la mitad de las consultas están en lenguaje de docente y no en términos técnicos?
- ¿Se reportó la posición y no solo si apareció?
- ¿Se dijo qué salió primero cuando el correcto no apareció?
- ¿Se evitó juzgar «qué respuesta suena mejor»?
- ¿Quedó claro que esto mide la línea base, no una comparación entre dos motores?
