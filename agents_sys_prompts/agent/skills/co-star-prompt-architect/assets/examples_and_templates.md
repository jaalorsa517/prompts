# Ejemplos y Plantillas de Implementación CO-STAR

Utiliza estos ejemplos aplicados como guía de formato al generar las respuestas.

## Ejemplo 1: Analista de Ciberseguridad
- **Context:** "Nuestra infraestructura en la nube AWS sufrió un pico de tráfico inusual desde IPs de Europa del Este a las 03:00 AM."
- **Objective:** "Redactar un informe preliminar de incidente para determinar si es un ataque DDoS o tráfico legítimo mal enrutado."
- **Style:** "Analista de Inteligencia de Amenazas (CTI) militar."
- **Tone:** "Clínico, urgente, basado en hechos, sin especulaciones."
- **Audience:** "El CISO y la junta directiva."
- **Response:** "Un reporte de una página con 3 secciones: Resumen Ejecutivo, IoCs preliminares y Siguientes Pasos Inmediatos."

## Ejemplo 2: Creador de Contenido Técnico
- **Context:** "Lanzamos una nueva API RESTful para procesamiento de pagos con criptomonedas."
- **Objective:** "Explicar cómo autenticarse y realizar el primer pago de prueba (Hello World)."
- **Style:** "Documentación oficial de Stripe."
- **Tone:** "Informativo, alentador, sumamente claro y estructurado."
- **Audience:** "Desarrolladores backend Junior y Mid-level."
- **Response:** "Un documento Markdown con una breve introducción, requisitos previos en viñetas y un bloque de código funcional en cURL y Node.js."

## Plantilla de Salida (Markdown sugerido)
```yaml
System_Prompt_Layer:
  Style: "[Definir el estilo o entidad a imitar]"
  Tone: "[Definir la actitud emocional/intelectual]"
  Audience: "[Definir el público objetivo y la calibración de complejidad]"
  Response_Rules: "[Definir el formato de salida global esperado]"

User_Prompt_Layer:
  Context: "[Definir la situación o información de fondo]"
  Objective: "[Definir la tarea exacta a ejecutar]"
  Response_Format: "[Opcional: formato específico para esta tarea]"
