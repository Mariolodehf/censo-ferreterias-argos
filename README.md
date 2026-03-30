# 🏗️ Censo Digital de Ferreterías en Colombia - Equipo 4

> [cite_start]"Reemplazamos semanas de visitas manuales con un sistema automático que muestra en tiempo real cuántas ferreterías hay y cuáles son oportunidad comercial para Argos." [cite: 5]

## 📖 1. Contexto y Problema
[cite_start]Actualmente, Cementos Argos no tiene una base de datos centralizada de ferreterías en Colombia[cite: 7]. [cite_start]La recolección de esta inteligencia de mercado depende 100% de visitas físicas de los asesores comerciales[cite: 8, 13]. 

Esto genera dolores críticos:
* [cite_start]**Datos heterogéneos:** La información llega en cuadernos, Excel y reportes verbales[cite: 8, 12].
* [cite_start]**Falta de cobertura:** El proceso manual limita la frecuencia y el alcance geográfico[cite: 6].
* [cite_start]**Análisis imposible:** Sin datos estructurados, no se puede segmentar ni analizar a la competencia[cite: 14].

## 💡 2. Nuestra Solución (MVP)
[cite_start]El **Equipo 4** ha diseñado un *Pipeline de Datos Automatizado* que extrae información de fuentes públicas (Google Maps API y RUES) [cite: 47, 48][cite_start], la limpia, y utiliza Inteligencia Artificial Generativa para clasificar el tamaño de cada negocio y calcular el `potencial_argos`[cite: 64, 65]. 

[cite_start]El resultado final se visualiza en un Dashboard interactivo con alcance nacional (32 departamentos)[cite: 4, 91].

## ⚙️ 3. Arquitectura y Herramientas
El sistema está construido con un enfoque modular:
* [cite_start]**Extracción:** Python, BeautifulSoup, Google Maps API y RUES[cite: 54, 119].
* [cite_start]**Limpieza y Estructuración:** Python (Pandas) y Geopy[cite: 68, 119].
* [cite_start]**Inteligencia Artificial:** Claude / OpenAI API (Clasificación y Estandarización)[cite: 68, 119].
* [cite_start]**Orquestación:** n8n (Automatización de flujos)[cite: 83, 119].
* [cite_start]**Visualización:** Streamlit (Dashboard y Mapa interactivo)[cite: 98, 119].

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
