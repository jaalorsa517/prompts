# Ejemplos y Plantillas de Implementación CARE

Utiliza estos ejemplos aplicados como guía de formato al generar las respuestas para el usuario.

## Ejemplo 1: Extracción de Entidades (NER)
- **Context:** "A continuación se presentan transcripciones de llamadas de servicio al cliente en bruto."
- **Action:** "Extrae el nombre del cliente, el número de producto mencionado y el motivo de la queja."
- **Result:** "Un arreglo de objetos JSON con las claves: `cliente`, `producto`, `motivo_queja`."
- **Example:** *Entrada:* "Hola, soy María López, llamo porque mi router modelo AX1500 no enciende desde ayer."
  *Salida:* `[{"cliente": "María López", "producto": "AX1500", "motivo_queja": "Dispositivo no enciende"}]`

## Ejemplo 2: Clasificación de Correos
- **Context:** "Recibimos correos electrónicos en la bandeja de soporte general."
- **Action:** "Clasifica el correo entrante en una de las siguientes categorías: 'Ventas', 'Soporte Técnico', 'Facturación' o 'Spam'."
- **Result:** "Devuelve únicamente la etiqueta de la categoría. Ningún texto adicional."
- **Example:**
  *Entrada:* "¿Cuáles son sus planes de precios para equipos de 10 personas?" -> *Salida:* `Ventas`
  *Entrada:* "Gane una tarjeta de regalo de $500 haciendo clic aquí." -> *Salida:* `Spam`

## Plantilla de Salida (Markdown sugerido)
```markdown
**[Context]**
{Definir la información de entrada o escenario base}

**[Action]**
{Definir la directiva clara y verbos imperativos}

**[Result]**
{Definir el formato técnico, longitud o estructura de la salida}

**[Example]**
- **Input:** "{Ejemplo de entrada 1}"
- **Output:** "{Ejemplo de salida exacta esperada 1}"
- **Input:** "{Ejemplo de entrada 2}"
- **Output:** "{Ejemplo de salida exacta esperada 2}"

**[Entrada del Usuario]**
{Aquí va la entrada real a procesar}
