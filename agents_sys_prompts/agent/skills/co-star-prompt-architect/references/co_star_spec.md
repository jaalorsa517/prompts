# Especificación del Framework CO-STAR

CO-STAR es una plantilla holística (Zero-Shot) excelente para definir la "personalidad" del modelo. Desglosa la identidad en tres vectores independientes, pero requiere una implementación cuidadosa para no mezclar instrucciones estáticas con contexto dinámico.

## Acrónimo y Desglose Estructural

* **C - Context (Contexto):** Información de fondo sobre el proyecto o la situación. *Naturaleza: Generalmente pertenece al User Prompt (dinámico).*
* **O - Objective (Objetivo):** La tarea principal y el fin último de la ejecución. *Naturaleza: Pertenece al User Prompt (dinámico).*
* **S - Style (Estilo):** El estilo de escritura a imitar (ej. referenciando profesiones, autores o marcas). *Naturaleza: System Prompt.*
* **T - Tone (Tono):** La actitud de la respuesta (ej. objetivo, persuasivo, clínico). *Naturaleza: System Prompt.*
* **A - Audience (Audiencia):** A quién va dirigido el texto, dictando vocabulario y sintaxis. *Naturaleza: System Prompt.*
* **R - Response (Respuesta / Formato):** El formato exacto y la estructura esperada. *Naturaleza: Híbrida (puede ser de Sistema si siempre es igual, o de Usuario si cambia por tarea).*

## Análisis Crítico Riguroso

1. **Precisión Taxonómica:** CO-STAR no es un System Prompt puro; agruparlo todo en una sola capa denota incomprensión de la arquitectura de LLMs. Es vital separar las variables (S, T, A) de las entradas (C, O).
2. **Fortalezas:** Superior a frameworks como CARE o RACE para definir la personalidad gracias a su triple vector (Estilo, Tono, Audiencia).
3. **Debilidades:** Omite variables de restricción negativa (Guardrails) fundamentales para entornos de producción seguros. Se recomienda mitigar esto reforzando la variable `Response`.
