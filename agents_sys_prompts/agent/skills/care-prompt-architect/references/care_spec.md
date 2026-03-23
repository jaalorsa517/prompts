# Especificación del Framework CARE

CARE es un framework táctico altamente efectivo para tareas directas, procesamiento de datos y flujos de trabajo donde se espera una transformación específica de la entrada. Sobresale en la implementación del patrón de diseño *Few-Shot Prompting*.

## Acrónimo y Desglose Estructural

* **C - Context (Contexto):** El escenario general, los datos de entrada o la información de fondo estrictamente necesaria para la tarea.
* **A - Action (Acción):** La directiva exacta. El verbo principal de la operación (ej. "Clasifica", "Extrae", "Traduce", "Resume").
* **R - Result (Resultado):** Las especificaciones del entregable. Incluye el formato de salida, longitud, tipo de archivo o estructura de datos.
* **E - Example (Ejemplo):** Pares de entrada/salida que demuestran exactamente cómo debe ejecutarse la acción y cómo debe verse el resultado.

## Análisis Crítico Riguroso

1. **Fortalezas Operativas:** Es excepcionalmente rápido de implementar para tareas de procesamiento en lote (batch processing) o llamadas a APIs donde el formato es crítico. La inclusión nativa de "Example" reduce drásticamente las alucinaciones de formato.
2. **Debilidades Arquitectónicas:** CARE carece de definición de Rol (Role), Tono (Tone) o Restricciones (Guardrails/Narrowing). 
3. **Mitigación:** Es recomendable que este framework se utilice como "User Prompt" dinámico dentro de un sistema que ya posee un "System Prompt" robusto gobernando el comportamiento general.
