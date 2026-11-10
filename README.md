# Proyecto_EH2025_ML_Caso2
Trabajo académico para el Módulo 3 - Análisis y visualización de datos masivos


![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![DuckDB](https://img.shields.io/badge/DuckDB-Fast_Data-yellow.svg)
![Machine Learning](https://img.shields.io/badge/Machine_Learning-XGBoost_%7C_Random_Forest-green.svg)
![Plotly](https://img.shields.io/badge/Plotly-Interactive_Plots-orange.svg)
![Status](https://img.shields.io/badge/Status-Completado-success.svg)

## Descripción del Proyecto
Este repositorio contiene el desarrollo del **Caso de Estudio 2** para el módulo de la Maestría en Análisis y Visualización de Datos. El proyecto aplica un stack tecnológico moderno de Ciencia de Datos para analizar los microdatos de la **Encuesta de Hogares 2025 (EH2025)** del Instituto Nacional de Estadística (INE) de Bolivia.

**Pregunta de investigación principal:**
> *¿Cómo se relacionan las condiciones de pobreza multidimensional con el acceso al empleo formal y la calidad del trabajo en Bolivia?*

## Stack Tecnológico
* **Ingesta y Procesamiento:** `DuckDB`, `Pandas` (con soporte `Dask` para out-of-core si es necesario).
* **Análisis Exploratorio (EDA):** `YData-Profiling` / `Sweetviz`.
* **Visualización Geoespacial e Interactiva:** `Folium`, `Plotly`.
* **Machine Learning & Clustering:** `Scikit-Learn`, `XGBoost` / `LightGBM`.
* **Interpretabilidad (XAI):** `SHAP`.
* **Storytelling:** `Quarto` (HTML5 / PDF).

## Estructura del Repositorio

El proyecto sigue estrictamente la siguiente estructura de directorios:

```text
Proyecto_EH2025_ML_Caso2/
├── data/                  # Microdatos crudos (.sav/.dta) o scripts de conexión (No subidos a GitHub por peso/privacidad)
├── notebooks/             # Jupyter Notebooks limpios, comentados y ejecutables
├── src/                   # Scripts de Python modulares (limpieza, features, modelado)
├── outputs/               # Reportes EDA en HTML y datasets procesados (.parquet/.csv)
├── docs/                  # Informe final de Storytelling (HTML5 / PDF) y recursos visuales
├── .gitignore             # Exclusión de archivos pesados y entornos virtuales
├── requirements.txt       # Dependencias exactas del proyecto
└── README.md              # Documentación técnica e instrucciones (Este archivo)
```

## Instrucciones de Ejecución

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/TU_USUARIO/Proyecto_EH2025_ML_Caso2.git
   cd Proyecto_EH2025_ML_Caso2
   ```

2. **Crear un entorno virtual (Recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instalar las dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Preparar los datos:**
   * Descarga los microdatos de la EH2025 desde el portal del INE y colócalos en la carpeta `data/`.

5. **Ejecutar el pipeline:**
   * Abre los notebooks ubicados en la carpeta `notebooks/` y ejecútalos en orden, o utiliza los scripts modulares de la carpeta `src/`.

## Resultados y Entregables Clave
* **Índice de Pobreza Multidimensional:** Construido a partir de variables de educación, salud e ingresos.
* **Modelo Predictivo:** Clasificación de la informalidad laboral (XGBoost/Random Forest) evaluado con métricas rigurosas (AUC-ROC, F1-Score).
* **Explainability (SHAP):** Identificación de los determinantes más fuertes del empleo formal en el contexto boliviano.
* **Segmentación Geoespacial:** Mapas interactivos mostrando la distribución de la vulnerabilidad por departamento.

## Consideraciones Éticas y Legales

* **Privacidad de los Datos:** Los datos utilizados en este estudio se encuentran estrictamente anonimizados por la entidad emisora. Bajo ninguna circunstancia se intenta o intentará reidentificar a los individuos u hogares participantes. El uso de estos microdatos es **estrictamente académico**.
* **Autoría:** Proyecto de carácter personal desarrollado para el programa de Maestría.

### Citación Obligatoria
Toda reproducción parcial o total de los análisis aquí presentados debe incluir la siguiente fuente formal:

> *"Fuente: Instituto Nacional de Estadística, Encuesta de Hogares 2025 - http://anda.ine.gob.bo/index.php/catalog/256. Fecha de acceso: [Noviembre de 2026]."*
