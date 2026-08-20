# 📊 Proyecto de Preparación y ETL - Padrón de Seguros de Salud y Vehículos

## 🎯 1. Objetivo del Proyecto
Este repositorio forma parte de mi portafolio como estudiante de Ingeniería en Sistemas y Analista de Datos. El objetivo principal es aplicar un proceso completo de **ETL (Extract, Transform, Load)** para limpiar y estructurar un padrón masivo de clientes. 

**Preguntas clave a resolver con estos datos:**
* ¿Cómo se distribuyen las primas anuales y existen valores atípicos (outliers) en los pagos?
* ¿Cuál es la proporción de clientes con daños previos en sus vehículos?
* ¿Existen discrepancias o errores de formato en los registros categóricos?

## 🛠️ 2. Stack Tecnológico
* **Python**: Lenguaje principal de procesamiento.
* **Pandas**: Limpieza, transformación y análisis exploratorio (EDA).
* **Jupyter Notebook**: Entorno de desarrollo interactivo.
* **Git & GitHub**: Control de versiones y documentación.

## 📂 Estructura del Repositorio
* `data/`: Carpeta (ignorada en Git) donde se aloja el dataset original de más de 381,000 registros.
* `ETL.ipynb`: Cuaderno principal con el código paso a paso y comentado.
* `README.md`: Resumen y conclusiones del proyecto.

## 🧹 3. Fases del Proceso ETL
1. **Extract (Extracción):** Carga eficiente del dataset masivo en un DataFrame estructurado mediante Pandas.
2. **Transform (Transformación y Auditoría):**
   * Verificación de la calidad de datos: 381,109 registros con **0 valores nulos**.
   * Auditoría de integridad: **0 registros duplicados**.
   * *(Próximamente)* Estandarización de variables de texto y tratamiento de outliers numéricos.
3. **Load (Carga):** *(Próximamente)* Exportación del padrón limpio a formato CSV, optimizado para ser consumido por herramientas de visualización o Machine Learning.

## 📊 4. Hallazgos y Conclusiones Preliminares
* **Estructura sólida:** El dataset base demostró una calidad excepcional de origen, sin faltantes ni registros repetidos, lo que agiliza la fase de normalización.
* **Distribución de variables:** El 75% de los afiliados abona primas anuales inferiores a $39,400.
* **Valores atípicos detectados:** Se identificó una prima máxima de $540,165 que requerirá aislamiento y análisis en la fase de transformación.

## 🚀 5. Cómo ejecutar este proyecto
1. Clona este repositorio: `git clone [URL_DE_TU_REPO]`
2. Instala la librería necesaria: `pip install pandas`
3. Ejecuta el archivo `ETL.ipynb` en tu entorno de Visual Studio Code o Jupyter local.

---
⌨️ Desarrollado por **Ysaac Salvatierra** | Estudiante de Ingeniería en Sistemas y Analista de Datos.
