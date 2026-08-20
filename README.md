# 📊 Análisis de Cross-Sell y Predicción de Seguros de Vehículos

## 🎯 1. Objetivo del Proyecto
El objetivo principal de este proyecto es analizar un padrón de clientes de seguros de salud para identificar qué perfiles tienen mayor probabilidad de adquirir un nuevo producto (seguro de vehículos). A través de un proceso de ETL y Análisis Exploratorio de Datos (EDA), busco extraer insights que permitan optimizar las campañas de venta cruzada (Cross-Sell).

**Preguntas clave de negocio a resolver:**
1. ¿Cómo influye el historial del vehículo (daños previos y antigüedad) en la tasa de conversión?
2. ¿Qué canales de venta son más efectivos y cómo varía su rendimiento según la edad del afiliado?
3. ¿Cómo impacta la tenencia previa de un seguro (`Previously_Insured`) en la tasa de conversión de la venta cruzada?

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
El análisis completo y el desarrollo gráfico se encuentran documentados en `EDA.ipynb`, arrojando los siguientes hallazgos estratégicos:
* **Impacto del Daño Previo:** Los clientes con historial de daños en el vehículo (`yes`) presentan una tasa de aceptación del **23.8%**, frente a un magro **0.5%** de aquellos con vehículos intactos (`no`), evidenciando que la venta cruzada se detona por la conciencia de riesgo y la experiencia de siniestro.
* **Efectividad de Canales:** El rendimiento comercial se concentra en canales clave, liderando la adopción los grupos etarios intermedios y adultos (especialmente los rangos de **31 a 40 años** y **41 a 50 años**).
* **Filtro de Póliza Previa:** La tenencia de un seguro previo marca una segmentación excluyente absoluta: la conversión cae al **0.09%** en clientes ya asegurados y asciende al **22.5%** en el segmento desprotegido, lo que exige excluir al primer grupo para optimizar el presupuesto publicitario.
* **Segmento de Alto Riesgo y Accionable:** Al combinar los antecedentes de daños con la ausencia de póliza previa, la tasa de conversión alcanza un **25.01%**. Como cierre del análisis, se automatizó un filtro que exporta la base limpia de **182,488 leads priorizados** (`leads_prioritarios_cross_sell.csv`) lista para la campaña de telemarketing.

## 🚀 6. Cómo ejecutar este proyecto
1. Clona este repositorio: `git clone https://github.com/YsaacSalvatierra99/Preparacion-y-ETL.git`
2. Instala las librerías: `pip install pandas matplotlib seaborn`
3. Ejecuta los cuadernos en Visual Studio Code o Jupyter local.
