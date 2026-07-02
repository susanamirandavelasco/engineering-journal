# Idea

Una buena arquitectura no consiste en ocultar todo; consiste en decidir cuidadosamente qué conocimiento pertenece a cada componente.

Hoy decidimos que:

* vector_store.py sabe hablar con ChromaDB.
* Retriever sabe interpretar los resultados de una búsqueda.
* Ninguno invade la responsabilidad del otro.

---
🐍 Python Corner #3

``` zip() ``` es una función muy utilizada en Python.

Si tienes:

```
nombres = ["Ana", "Luis"]

edades = [30, 28]
```

Entonces:

```
for nombre, edad in zip(nombres, edades):
    print(nombre, edad)
```

produce:

```
Ana 30

Luis 28
```

En nuestro caso es perfecto porque Chroma devuelve tres listas paralelas.

---
🐍 Python Corner #4

Hay un principio útil para recordar:

Variables locales → crea la lista con [].

```
def mi_funcion():
    lista = []
```

Atributos de una dataclass → usa default_factory.

```
@dataclass
class MiClase:
    lista: list = field(default_factory=list)
```

Parámetros de funciones → nunca hagas esto:

```
def agregar(item, lista=[]):   # ❌
```

Porque ocurre exactamente el mismo problema que en las dataclasses.
