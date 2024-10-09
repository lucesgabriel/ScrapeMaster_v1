Universal Web Scraper 🦑

Este proyecto es una aplicación universal de scraping web que permite extraer datos de sitios web y convertirlos en un formato estructurado. Utiliza diversas APIs de inteligencia artificial para mejorar la detección de paginación y generar datos estructurados en formato JSON o CSV.

Estructura del Proyecto
markdown
Copy code
└── ./  
    ├── assets.py  
    ├── pagination_detector.py  
    ├── requirements.txt  
    ├── scraper.py  
    └── streamlit_app.py  
Descripción de Archivos:
assets.py: Contiene constantes y variables de configuración que se utilizan en diferentes partes de la aplicación. Ejemplos incluyen configuraciones de agentes de usuario, opciones de modo sin cabeza y precios de los modelos de IA.

pagination_detector.py: Módulo para detectar elementos de paginación en el contenido de sitios web. Utiliza modelos de IA para extraer información y calcular los precios de las operaciones basadas en el número de tokens utilizados.

scraper.py: Módulo principal que maneja la extracción de datos de los sitios web, incluyendo la configuración de Selenium, limpieza de HTML y conversión a formato markdown. También permite el procesamiento de datos con modelos de IA como OpenAI, Google Gemini y Groq.

streamlit_app.py: Aplicación principal de Streamlit que proporciona una interfaz gráfica para el scraping. Los usuarios pueden introducir URLs, definir campos a extraer y configurar la paginación. Los resultados se pueden descargar en formato JSON o CSV.

requirements.txt: Lista de dependencias necesarias para ejecutar el proyecto.

Requisitos del Sistema
Para ejecutar este proyecto, asegúrate de tener los siguientes componentes instalados:

Python 3.8+
Google Chrome (para Selenium)
ChromeDriver (configurado en el PATH)
Instalación de dependencias: Utiliza el siguiente comando para instalar todas las dependencias del proyecto.
bash
Copy code
pip install -r requirements.txt
Cómo Ejecutar la Aplicación
Configura el entorno:

Crea un archivo .env en el directorio raíz con tus claves API para OpenAI, Google y Groq.
bash
Copy code
OPENAI_API_KEY=tu_clave_api_openai
GOOGLE_API_KEY=tu_clave_api_google
GROQ_API_KEY=tu_clave_api_groq
Inicia la aplicación:

Ejecuta el siguiente comando para iniciar la aplicación de Streamlit:
bash
Copy code
streamlit run streamlit_app.py
Uso de la aplicación:

Ingresa una o más URLs en la barra lateral.
Define los campos que deseas extraer como etiquetas.
Activa la detección de paginación si es necesario.
Haz clic en "Scrape" para iniciar el scraping.
Descarga los resultados:

Descarga los datos extraídos en formato JSON o CSV desde la interfaz de usuario.
Modelos Soportados
Este proyecto soporta varios modelos de IA para realizar las tareas de extracción y detección de paginación:

OpenAI: Modelos como gpt-4o-mini y gpt-4o-2024-08-06.
Google Gemini: Modelo gemini-1.5-flash.
Groq Llama: Modelos Llama3.1 8B y Groq Llama3.1 70b.
Cada modelo tiene costos asociados según los tokens utilizados, que se calculan automáticamente y se muestran en la aplicación.

Funcionalidades
Extracción de datos: Extrae información estructurada de sitios web usando IA.
Detección de paginación: Detecta elementos de paginación y sigue enlaces a otras páginas.
Conversión de HTML a Markdown: Limpia el HTML y lo convierte a formato Markdown para una mejor legibilidad.
Compatibilidad con múltiples modelos de IA: Selección de modelos de IA para la extracción de datos.
Licencia
Este proyecto está bajo la MIT License.

Contacto
Si encuentras algún error o tienes sugerencias, no dudes en crear un issue en GitHub.
