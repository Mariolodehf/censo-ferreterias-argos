# 🏗️ Censo Digital de Ferreterías en Colombia - Equipo 4

> "Reemplazamos semanas de visitas manuales con un sistema automático que muestra en tiempo real cuántas ferreterías hay y cuáles son oportunidad comercial para Argos."

## 📖 1. Contexto y Problema
Actualmente, Cementos Argos no tiene una base de datos centralizada de ferreterías en Colombia. La recolección de esta inteligencia de mercado depende 100% de visitas físicas de los asesores comerciales. 

Esto genera dolores críticos:
* **Datos heterogéneos:** La información llega en cuadernos, Excel y reportes verbales.
* **Falta de cobertura:** El proceso manual limita la frecuencia y el alcance geográfico.
* **Análisis imposible:** Sin datos estructurados, no se puede segmentar ni analizar a la competencia.

## 💡 2. Nuestra Solución (MVP)
El **Equipo 4** ha diseñado un *Pipeline de Datos Automatizado* que extrae información de fuentes públicas (Google Maps API y RUES), la limpia, y utiliza Inteligencia Artificial Generativa para clasificar el tamaño de cada negocio y calcular el `potencial_argos`. 

El resultado final se visualiza en un Dashboard interactivo con alcance nacional (32 departamentos).

## ⚙️ 3. Arquitectura y Herramientas
El sistema está construido con un enfoque modular:
* **Extracción:** Python, BeautifulSoup, Google Maps API y RUES.
* **Limpieza y Estructuración:** Python (Pandas) y Geopy.
* **Inteligencia Artificial:** Claude / OpenAI API (Clasificación y Estandarización).
* **Orquestación:** n8n (Automatización de flujos).
* **Visualización:** Streamlit (Dashboard y Mapa interactivo).

## 📂 4. Estructura del Repositorio
```text
📦 censo-ferreterias-argos
 ┣ 📂 1_scraper            # Scripts de Python para extracción de Google Maps y RUES
 ┣ 📂 2_procesamiento      # Scripts con Pandas para limpieza y geocodificación
 ┣ 📂 3_ia_prompts         # Documentación y lógica de prompts para categorización
 ┣ 📂 4_n8n_pipeline       # Archivos JSON exportados del flujo de automatización
 ┣ 📂 5_dashboard          # Código de la aplicación web en Streamlit
 ┣ 📂 docs                 # Informe técnico en PDF y propuestas de herramientas
 ┣ 📜 README.md            # Documentación principal del proyecto
 ┗ 📜 requirements.txt     # Dependencias de Python (pandas, requests, googlemaps, etc.)
