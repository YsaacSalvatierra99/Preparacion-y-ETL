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
* **Matplotlib & Seaborn**: Visualización de datos y detección de patrones.
* **Jupyter Notebook**: Entorno de desarrollo para análisis narrativo e interactivo.

## 📖 3. Diccionario de Datos
Para comprender el padrón de afiliados, a continuación se detallan las variables del dataset:

| Columna | Descripción |
| :--- | :--- |
| **id** | Identificador único del afiliado. |
| **Gender** | Género del afiliado. |
| **Age** | Edad biológica. |
| **Age_Group** | Rango de edad segmentado (Feature Engineering propio). |
| **Driving_License** | `1`: Tiene licencia de conducir, `0`: No tiene. |
| **Region_Code** | Código anonimizado de la región donde reside el cliente. |
| **Previously_Insured**| `1`: El cliente ya tiene seguro de auto, `0`: No tiene. |
| **Vehicle_Age** | Antigüedad del vehículo (ej. `< 1 Year`, `1-2 Year`). |
| **Vehicle_Damage** | `yes`: El vehículo tuvo daños en el pasado, `no`: Sin daños. |
| **Annual_Premium** | Prima anual (monto en $) que paga por su seguro de salud actual. |
| **Policy_Sales_Channel**| Código anonimizado del canal de contacto (ej. correo, teléfono, presencial). |
| **Vintage** | Días de antigüedad del cliente en la aseguradora. |
| **Response** | Variable objetivo (`1`: Aceptó la oferta de seguro de auto, `0`: La rechazó). |

## 🧹 4. Fases del Proceso: Preparación y ETL
**Fase completada.** El proceso detallado se encuentra en `ETL.ipynb`:
* **Auditoría de calidad:** Verificación de 381,109 registros confirmando **0 valores nulos** y **0 duplicados**.
* **Transformación:** Estandarización de columnas de texto a minúsculas.
* **Tratamiento de Outliers:** Aislamiento y eliminación de primas anuales extremas (> $500,000) para no distorsionar métricas.
* **Feature Engineering:** Creación de la columna categórica `Age_Group`.
* **Exportación:** Generación del archivo final optimizado `train_clean.csv`.

## 📊 5. Análisis Exploratorio (EDA) e Insights de Negocio
* **Impacto del Daño Previo:** Se identificó que el antecedente de siniestros o daños en el vehículo es el principal motor de conversión. Los clientes con historial de daños (`yes`) presentan una tasa de aceptación del **23.8%**, en contrastada oposición al **0.5%** de aquellos con vehículos intactos (`no`). 
* **Acción sugerida:** Optimizar el presupuesto de marketing focalizando las campañas de venta cruzada exclusivamente en segmentos que ya hayan experimentado incidentes o que posean mayor propensión al riesgo. *(Análisis completo en desarrollo dentro de `EDA.ipynb`)*.

## 🚀 6. Cómo ejecutar este proyecto
1. Clona este repositorio: `git clone https://github.com/YsaacSalvatierra99/Preparacion-y-ETL.git`
2. Instala las librerías: `pip install pandas matplotlib seaborn`
3. Ejecuta los cuadernos en Visual Studio Code o Jupyter local.
