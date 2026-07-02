# Concepto

Un RAG no solo necesita algoritmos; necesita modelos de datos claros que definan cómo colaboran sus componentes.

## Ingeniería

Las dataclasses permiten representar información estructurada de forma legible, tipada y fácil de mantener.

## Diseño

RetrievedChunk representa una unidad de conocimiento recuperada.

RetrievalResult representa el resultado completo de una operación de búsqueda.

La diferencia parece sutil, pero expresa mucho mejor la intención del sistema.

---

# Concepto

Un Retriever no responde preguntas. Recupera contexto. Eso es todo.

# Ingeniería

Antes de implementar una clase, conviene diseñar su interfaz pública. 

El resto del sistema dependerá de esa interfaz, no de los detalles internos.

# Diseño

Una clase con una única responsabilidad es más fácil de probar, mantener y reemplazar.

---

🐍 Python Corner #1: 
Objetos mutables

En Python:

```[]``` crea un objeto mutable.

Si ese objeto se usa como valor por defecto, puede terminar siendo compartido entre instancias.

Por eso existe:

``` field(default_factory=list) ``` que crea una lista nueva para cada objeto.

🐍 Python Corner #2

Hoy apareció algo muy común en Python:

```raise NotImplementedError```

En Java probablemente habrías escrito una interfaz o una clase abstracta.

En Python, muchas veces empezamos definiendo el contrato y dejamos claro que aún no hay implementación.

Es una forma simple de decir:

"Esta función existe, pero todavía no está construida."

Más adelante aprenderemos alternativas más sofisticadas (ABC, Protocol), pero por ahora esta solución mantiene el proyecto sencillo y muy legible.

