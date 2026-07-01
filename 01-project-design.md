# Sesión 1

## Objetivo

Diseñar la arquitectura del sistema RAG.

---

## Conceptos aprendidos

- Retrieval y Generation son etapas distintas.
- El LLM nunca recibe embeddings.
- Los embeddings solo sirven para recuperar contexto.

---

## Decisiones de diseño

- Proyecto independiente del Semantic Search.
- Retriever desacoplado.
- Uso de dataclasses.

---

## Dudas que surgieron

- ¿Cómo medir si el Retrieval fue suficientemente bueno?

---

## Ideas para investigar después

- Retrieval Evaluation
- Re-ranking
- Hybrid Search
