# Especificación del Framework RACE

RACE es un framework de diseño de prompts equilibrado, ideal para tareas cotidianas, asistentes virtuales y flujos de trabajo donde se necesita una salida rápida pero con un tono y formato controlados.

## Acrónimo y Desglose Estructural

* **R - Role (Rol):** La persona, experto o entidad que el modelo de lenguaje debe asumir. Establece el tono base y el nivel de conocimiento técnico.
* **A - Action (Acción):** La tarea específica que se debe realizar. Debe ser un verbo imperativo directo (ej. "Redacta", "Analiza", "Depura").
* **C - Context (Contexto):** La información de fondo, el escenario actual o los datos de entrada sobre los cuales se aplicará la acción.
* **E - Expectation (Expectativa):** El resultado deseado. Define el formato, la estructura, el tono específico y cualquier restricción o límite crítico (actúa como un guardrail básico).

## Análisis Crítico Riguroso

1. **Fortalezas Operativas:** Es más completo que CARE al incluir un `Role`, lo que mejora drásticamente el tono y el vocabulario de la respuesta. Es más ágil que RISEN, haciéndolo perfecto para interacciones "Zero-Shot" rápidas.
2. **Debilidades Arquitectónicas:** Al comprimir el formato, las restricciones y el objetivo final en una sola variable (`Expectation`), puede quedarse corto para agentes autónomos complejos o tareas de alto riesgo que requieran un "Chain of Thought" explícito (como la variable `Steps` en RISEN).
3. **Casos de Uso Ideales:** Generación de contenido, revisiones de código rápidas, resúmenes ejecutivos y asistentes de chat de propósito general.
