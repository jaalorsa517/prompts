# Especificación del Framework RISEN

RISEN es una arquitectura de System Prompt de grado de producción que busca estructurar el comportamiento del modelo, reducir errores lógicos y establecer límites seguros.

## Acrónimo y Desglose Estructural

* **R - Role (Rol):** La identidad operativa del agente. Debe ser inmutable durante toda la sesión.
* **I - Instructions (Instrucciones principales):** El mandato general del agente. ¿Qué hace a grandes rasgos?
* **S - Steps (Pasos metodológicos):** Induce al "Chain of Thought" (Razonamiento en cadena). Fuerza al modelo a procesar internamente en una secuencia lógica antes de generar la salida. Reduce drásticamente los errores lógicos y matemáticos.
* **E - End Goal (Objetivo Final):** Lo que se busca lograr. *Nota arquitectónica:* Es una variable efímera. Si se codifica rígidamente en el backend, el agente solo sirve para una tarea. Considerar mover al User Prompt si se busca flexibilidad.
* **N - Narrowing (Restricciones / Delimitación):** Límites y Guardrails. Es vital para prevenir inyecciones y alucinaciones. Define el formato exacto de salida y los juicios prohibidos.

## Análisis Crítico
RISEN es altamente efectivo porque la inclusión de "Narrowing" protege al sistema, mientras que "Steps" mejora la capacidad de razonamiento. La clave de un buen diseño con RISEN es la correcta separación entre el sistema base (R, I, S, N) y la ejecución variable (E).
