# 🏠 Argenprop Scraper

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg) ![Status](https://img.shields.io/badge/Status-Paginación_Corregida-brightgreen.svg)

Este scraper avanzado automatiza la recolección de datos de **Argenprop** (Departamentos en CABA). Utiliza una lógica de navegación por parámetros (`?pagina-X`) y realiza una extracción profunda de cada aviso para categorizar características mediante inteligencia de texto.

## 📂 Estructura del Proyecto

```text
argenprop_scrapper/
├── scrapper.py       # Script principal  
├── README.md         # Documentación  
├── .gitignore        # Archivos excluidos de Git  
└── output/           # Carpeta auto-generada con los resultados  
```

## ✨ Características de esta Versión

- Paginación Dinámica: corregida para navegar mediante parámetros de consulta, evitando el bucle infinito en la página 1.  
- Carpeta de Salida: los resultados se guardan automáticamente en /output con un timestamp único.  
- Formato TSV (Tab Separated Values): fundamental para descripciones largas. Al usar tabuladores en lugar de comas, se garantiza que el archivo se abra correctamente en Excel sin desfasar celdas.  
- Smart Features (0/1): columnas automáticas para Amenities, Losa Radiante, Aire Acondicionado, Apto Crédito, Cochera, Seguridad, Luminosidad y Balcón Aterrazado.

## 🛠️ Instalación

Instalá las dependencias ejecutando:
```bash
pip install requests beautifulsoup4 pandas
```

## 🚀 Cómo abrir los resultados en Excel

Dado que el archivo de salida es .tsv, seguí estos pasos para que Excel no rompa el formato:  
1. Abrí Excel.  
2. Andá a la pestaña Datos.  
3. Seleccioná Obtener datos (o De texto/CSV).  
4. Elegí el archivo dentro de la carpeta output.  

En el asistente configurá:  
  Origen de archivo: 65001 Unicode UTF-8.  
  Delimitador: Tabulación.

## ⚠️ Configuración de Paginación

Para cambiar cuántas páginas querés procesar, editá el final de scrapper.py y ajustá el parámetro max_pages en la función run_scrapper.

---
Desarrollado para análisis de mercado inmobiliario.
