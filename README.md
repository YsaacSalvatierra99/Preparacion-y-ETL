# 📊 Proyecto de Preparación y ETL - Padrón de Seguros y Afiliados

## 📌 Descripción del Proyecto
Este repositorio forma parte de mi portafolio como analista de datos y estudiante de Ingeniería en Sistemas. El objetivo principal de este proyecto es realizar el proceso completo de **ETL (Extract, Transform, Load)** y la auditoría de calidad de datos sobre un dataset de seguros de salud y vehículos, utilizando Python y la librería Pandas.

## 🛠️ Tecnologías y Herramientas Utilizadas
* **Python**: Lenguaje principal de programación.
* **Pandas**: Manipulación, limpieza y análisis exploratorio de datos.
* **Jupyter Notebook (.ipynb)**: Entorno interactivo de desarrollo estructurado en celdas.
* **Visual Studio Code**: Entorno de desarrollo local.
* **Git & GitHub**: Control de versiones y alojamiento de código en la nube.

## 📂 Estructura del Repositorio
* `ETL.ipynb`: Cuaderno principal con el código paso a paso de la extracción, auditoría y limpieza de los datos.
* `.gitignore`: Configuración para excluir archivos locales innecesarios o pesados.

## 🔍 Fases del Proyecto (ETL)
1. **Extract (Extracción):** Carga eficiente del dataset masivo (más de 381,000 registros) en un DataFrame estructurado mediante Pandas.
2. **Transform (Transformación y Auditoría):**
   * Inspección de tipos de datos y estructuras mediante `df.info()`.
   * Verificación exhaustiva de valores nulos o celdas vacías.
   * Auditoría de registros duplicados para asegurar la integridad de la base.
3. **Load (Carga):** Preparación del entorno y documentación para la exportación de los datos limpios hacia un destino final listo para análisis avanzados o modelos predictivos.

## 📊 Hallazgos del Análisis Preliminar
Tras realizar la auditoría inicial de los datos, se obtuvieron las siguientes conclusiones:
- **Calidad de datos:** El dataset se encuentra completo, con 381,109 registros y 0 valores nulos en todas sus columnas.
- **Integridad:** Se realizó un conteo de duplicados (resultado: 0), confirmando que el padrón es consistente.
- **Estructura:** Se identificaron variables categóricas (como 'Gender' o 'Vehicle_Damage') y numéricas (como 'Annual_Premium') listas para ser transformadas para futuros modelos.



---
⌨️ Desarrollado con 💻 por **Ysaac Salvatierra** | Estudiante de Ingeniería en Sistemas y Analista de Datos Junior.



