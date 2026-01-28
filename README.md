🏠 Argenprop Scraper Pro v3
Este scraper avanzado automatiza la recolección de datos de Argenprop (Departamentos en CABA). Utiliza una lógica de navegación por parámetros (?pagina-X) y realiza una extracción profunda de cada aviso para categorizar características mediante inteligencia de texto.

✨ Características de esta Versión
Paginación Dinámica: Corregida para navegar mediante parámetros de consulta, evitando el bucle infinito en la página 1.

Carpeta de Salida: Los resultados se guardan automáticamente en la subcarpeta output con un timestamp único.

Formato TSV (Tab Separated Values): Fundamental para descripciones largas. Al usar tabuladores en lugar de comas, se garantiza que el archivo se abra perfectamente en Excel sin que las celdas se desfasen.

Smart Features (0/1): Columnas automáticas para detectar Amenities, Losa Radiante, Aire Acondicionado, Apto Crédito, Cochera, Seguridad, Luminosidad y Balcón Aterrazado.

Address Parser: Divide automáticamente la dirección en Calle, Altura y Piso.

🛠️ Instalación
Instalá las dependencias necesarias mediante la terminal ejecutando: pip install requests beautifulsoup4 pandas

🚀 Cómo abrir los resultados en Excel
Dado que el archivo de salida es .tsv, seguí estos pasos para que Excel mantenga el formato correcto:

Abrí Excel.

Ir a la pestaña Datos.

Seleccionar Obtener datos de texto/CSV.

Elegir el archivo dentro de la carpeta output.

Configuración crítica en el asistente:

Origen de archivo: 65001: Unicode (UTF-8).

Delimitador: Tabulación.

⚠️ Configuración de Paginación
Para cambiar la cantidad de páginas a scrapear, editá el final de tu archivo scrapper.py en la función run_scrapper(max_pages=X). Cambiá ese número según tu necesidad (por ejemplo, max_pages=10).

Desarrollado para análisis de mercado inmobiliario.
