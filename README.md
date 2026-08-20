# 📊 Análisis de Cross-Sell y Predicción de Seguros de Vehículos

## 🎯 1. Objetivo del Proyecto
El objetivo principal de este proyecto es analizar un padrón de clientes de seguros de salud para identificar qué perfiles tienen mayor probabilidad de adquirir un nuevo producto (seguro de vehículos). A través de un proceso de ETL y Análisis Exploratorio de Datos (EDA), busco extraer insights que permitan optimizar las campañas de venta cruzada (Cross-Sell).

**Preguntas clave de negocio a resolver:**
1. ¿Cómo influye el historial del vehículo (daños previos y antigüedad) en la tasa de conversión?
2. ¿Qué canales de venta son más efectivos y cómo varía su rendimiento según la edad del afiliado?
3. ¿Cuál es la distribución de la Prima Anual por región y cómo afecta la sensibilidad al precio en la aceptación de la oferta?

## 🛠️ 2. Stack Tecnológico
* **Python**: Lenguaje principal de procesamiento.
* **Pandas**: Limpieza, transformación estructurada y Feature Engineering.
* **Jupyter Notebook**: Entorno de desarrollo para análisis narrativo e interactivo.
* **Git & GitHub**: Control de versiones y documentación del portfolio.

## 📂 Estructura del Repositorio
* `data/`: Directorio alojando el dataset original de +381,000 registros (ignorado por peso).
* `ETL.ipynb`: Cuaderno principal documentado paso a paso con la extracción, transformación y limpieza de los datos.
* `README.md`: Resumen ejecutivo y hallazgos del proyecto.

## 🧹 3. Fases del Proceso (ETL y Preparación)
1. **Extract (Extracción):** Carga eficiente del dataset en un DataFrame estructurado.
2. **Transform (Transformación y Limpieza):**
   * Auditoría de calidad: 381,109 registros con **0 valores nulos** y **0 duplicados**.
   * Estandarización de columnas categóricas de texto (conversión a minúsculas).
   * Identificación y aislamiento de valores atípicos extremos (Primas Anuales > $500,000).
3. **Load (Carga):** *(Próximamente)* Exportación del padrón limpio y segmentado.

## 📊 4. Hallazgos Preliminares
* El padrón inicial demostró alta consistencia e integridad, sin faltantes de datos.
* El 75% de los clientes abonan primas anuales inferiores a $39,400.
* La variable objetivo (`Response`) indica el interés real en la oferta complementaria, permitiendo una segmentación directa del riesgo.

## 🚀 5. Cómo ejecutar este proyecto
1. Clona este repositorio: `git clone [URL_DE_TU_REPO]`
2. Instala la librería necesaria: `pip install pandas`
3. Ejecuta el archivo `ETL.ipynb` en tu entorno de Visual Studio Code o Jupyter local.

---
⌨️ Desarrollado por **Ysaac Salvatierra** | Estudiante de Ingeniería en Sistemas y Analista de Datos.
