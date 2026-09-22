Un script interactivo de línea de comandos en Python que consume la API REST pública de Open Trivia Database para extraer y mostrar preguntas de cultura general generadas aleatoriamente, basándose en la cantidad solicitada por el usuario.

## Arquitectura y Lógica Integrada

El script está dividido en dos funciones principales:
* `trivia_fetch(numero)`: Se encarga de construir la URL dinámica, realizar la petición HTTP GET y parsear la respuesta JSON. **Nota de desarrollo:** Esta función incluye una mutación intencional del objeto JSON resultante (agregando la clave `number`). Esta modificación es un requerimiento estricto para asegurar la compatibilidad y validación exitosa contra la suite de pruebas local (`test.py`).
* `main()`: Maneja la interacción directa con el usuario, captura el input por consola, invoca la petición y procesa la iteración sobre el array de resultados (`results`) para imprimir exclusivamente el texto de las preguntas.


## Instalación

1. Clona este repositorio o asegúrate de tener los archivos `script.py` y `test.py` en tu directorio local.
2. Abre una terminal y navega hasta la ruta del proyecto.
3. Si no tienes instalada la librería requerida, ejecútala en tu entorno virtual:

   ```bash
   pip install requests
