*📊Análisis de Clientes — ConnectaTel

## 🇪🇸 ES Español

## Descripción del Proyecto

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de **ConnectaTel**, una empresa de telecomunicaciones en Latinoamérica, utilizando información histórica registrada hasta el año 2024.

A partir de los datos de clientes, planes y uso de servicios, se realizó un proceso de exploración, limpieza, análisis estadístico y segmentación para identificar patrones de consumo, detectar comportamientos atípicos y generar recomendaciones estratégicas para el negocio.

## Objetivos del Proyecto

- Evaluar la calidad de los datos disponibles.
- Identificar y corregir valores nulos, valores sentinela y fechas inválidas.
- Analizar el comportamiento de uso de llamadas y mensajería.
- Detectar valores atípicos (*outliers*).
- Construir indicadores de uso por cliente.
- Segmentar a los clientes según su nivel de uso y grupo etario.
- Generar recomendaciones comerciales basadas en evidencia.

## Datasets Utilizados

### `plans.csv`

Contiene información de los planes ofrecidos por la compañía:

- Nombre del plan
- Precio mensual
- Minutos incluidos
- GB incluidos
- Costo por excedentes

### `users_latam.csv`

Contiene información demográfica y comercial de los clientes:

- Identificador de usuario
- Edad
- Ciudad
- Fecha de registro
- Tipo de plan
- Fecha de cancelación (*churn*)

### `usage.csv`

Contiene el histórico de uso de los servicios:

- Identificador de usuario
- Fecha de uso
- Tipo de actividad: llamada o mensaje
- Duración de llamadas
- Longitud de mensajes

# Análisis Exploratorio de Datos (EDA)

Se realizó una exploración inicial de los datasets con el propósito de comprender su estructura, evaluar la calidad de la información e identificar patrones relevantes en el comportamiento de los clientes.

### Principales tareas

- Carga y revisión inicial de los datasets.
- Revisión de la estructura de los datos.
- Validación de tipos de datos.
- Identificación y análisis de valores nulos.
- Revisión de valores sentinela.
- Validación de fechas.
- Análisis de variables demográficas y de consumo.
- Identificación de valores atípicos mediante herramientas estadísticas y visualizaciones.

# Calidad y Limpieza de Datos

Durante la etapa de calidad de datos se identificaron diferentes situaciones que podían afectar el análisis.

### Problemas identificados

- Valores nulos en la variable `city`.
- Fechas de cancelación (`churn_date`) faltantes.
- Valores sentinela `"?"` en la variable ciudad.
- Fechas futuras correspondientes a 2026, inconsistentes con el alcance temporal del proyecto.
- Valores nulos asociados al tipo de actividad registrada.

### Tratamiento aplicado

Se realizaron las siguientes acciones:

- Conversión de fechas al formato `datetime`.
- Reemplazo de valores sentinela por valores nulos.
- Corrección de fechas fuera del rango establecido para el proyecto.
- Conservación de valores nulos cuando estaban explicados por la naturaleza de los datos.

Este proceso permitió mejorar la consistencia de los datos antes de realizar el análisis estadístico y la segmentación de clientes.

# Construcción de Variables e Indicadores

Para facilitar el análisis del comportamiento individual de los clientes, se construyeron indicadores agregados por usuario.

### Indicadores generados

- Cantidad de mensajes enviados.
- Cantidad de llamadas realizadas.
- Total de minutos consumidos.

Estos indicadores permitieron comparar los niveles de utilización de los servicios y posteriormente construir segmentos de clientes.

# Análisis Estadístico

Se realizó un análisis descriptivo de las principales variables relacionadas con el comportamiento de los usuarios.

### Variables analizadas

- Edad.
- Cantidad de mensajes.
- Cantidad de llamadas.
- Minutos consumidos.

### Técnicas utilizadas

- Medias.
- Medianas.
- Cuartiles.
- Histogramas.
- Boxplots.

El análisis permitió identificar la distribución de los datos, diferencias en los niveles de consumo y posibles valores atípicos.

# Segmentación de Clientes

Se desarrolló una segmentación de los usuarios utilizando dos dimensiones principales: **nivel de uso de los servicios y grupo etario**.

### Segmentación por nivel de uso

- **Bajo uso**
- **Uso medio**
- **Alto uso**

### Segmentación por edad

- **Joven:** menor de 30 años.
- **Adulto:** entre 30 y 59 años.
- **Adulto Mayor:** 60 años o más.

Esta segmentación permitió identificar diferentes perfiles de consumidores y establecer oportunidades comerciales según sus patrones de comportamiento.

# Hallazgos Clave

## Calidad de Datos

- Se identificaron valores faltantes en la variable `city`.
- La mayoría de los valores nulos en `churn_date` corresponden a clientes activos.
- Se detectaron registros con fechas futuras de 2026, inconsistentes con el alcance temporal definido para el análisis.

## Uso de Servicios

- La mayoría de los usuarios presenta un **nivel de uso medio**.
- El tráfico de llamadas y mensajes muestra distribuciones similares entre los planes **Básico y Premium**.
- Existen usuarios con consumos excepcionalmente altos, especialmente en minutos de llamada.

## Segmentación

- Predomina el segmento de **adultos**.
- El grupo de **uso medio** concentra la mayor cantidad de clientes.
- Los usuarios de alto consumo representan una oportunidad para productos premium o paquetes especializados.

# Recomendaciones Estratégicas

A partir de los resultados obtenidos, se plantean las siguientes recomendaciones:

- Diseñar estrategias comerciales enfocadas en usuarios de **uso medio** para incentivar migraciones hacia planes superiores.
- Crear beneficios diferenciales para clientes de **alto consumo**.
- Fortalecer los controles de calidad para evitar registros con fechas inconsistentes.
- Implementar un monitoreo continuo de valores atípicos para identificar oportunidades de negocio o posibles errores operativos.
- Utilizar la segmentación de clientes para desarrollar campañas comerciales más específicas.

# Herramientas Utilizadas

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab**
- **GitHub**

# Cómo Ejecutar el Proyecto

### 1. Clonar el repositorio


# 📊 Customer Analysis — ConnectaTel

## 🇺🇸 US English

## Project Description

This project aims to analyze customer behavior at **ConnectaTel**, a telecommunications company operating in Latin America, using historical information recorded through 2024.

Based on customer, plan, and service usage data, an exploratory, data cleaning, statistical analysis, and customer segmentation process was conducted to identify consumption patterns, detect anomalous behavior, and generate strategic business recommendations.

## Project Objectives

- Evaluate the quality of the available data.
- Identify and correct missing values, sentinel values, and invalid dates.
- Analyze call and messaging usage patterns.
- Detect outliers in customer consumption.
- Build customer-level usage indicators.
- Segment customers according to usage level and age group.
- Generate evidence-based business recommendations.

## Datasets Used

### `plans.csv`

Contains information about the plans offered by the company:

- Plan name
- Monthly price
- Included minutes
- Included GB
- Overage costs

### `users_latam.csv`

Contains demographic and commercial customer information:

- User ID
- Age
- City
- Registration date
- Plan type
- Churn date

### `usage.csv`

Contains historical service usage data:

- User ID
- Usage date
- Activity type: call or message
- Call duration
- Message length

# Exploratory Data Analysis (EDA)

An exploratory analysis was performed to understand the structure of the datasets, evaluate data quality, and identify relevant patterns in customer behavior.

### Main Tasks

- Loaded and reviewed the datasets.
- Reviewed the data structure.
- Validated data types.
- Identified and analyzed missing values.
- Reviewed sentinel values.
- Validated date fields.
- Analyzed demographic and usage variables.
- Identified outliers using statistical techniques and visualizations.

# Data Quality and Cleaning

Several data quality issues were identified during the analysis.

### Issues Identified

- Missing values in the `city` variable.
- Missing churn dates (`churn_date`).
- Sentinel values `"?"` in the city variable.
- Future dates from 2026, which were inconsistent with the project's time scope.
- Missing values associated with the recorded activity type.

### Data Cleaning Process

The following actions were performed:

- Converted date variables to `datetime` format.
- Replaced sentinel values with missing values.
- Corrected dates outside the project's defined time range.
- Preserved missing values when they were explained by the nature of the data.

This process improved data consistency before performing statistical analysis and customer segmentation.

# Feature Engineering and Customer Metrics

Customer-level indicators were created to facilitate the analysis of individual service usage.

### Metrics Created

- Number of messages sent.
- Number of calls made.
- Total minutes consumed.

These indicators were used to compare service usage levels and build customer segments.

# Statistical Analysis

Descriptive statistical analysis was performed on the main variables related to customer behavior.

### Variables Analyzed

- Age.
- Number of messages.
- Number of calls.
- Total minutes consumed.

### Techniques Used

- Mean.
- Median.
- Quartiles.
- Histograms.
- Boxplots.

The analysis helped identify data distributions, differences in consumption levels, and potential outliers.

# Customer Segmentation

Customers were segmented using two main dimensions: **service usage level and age group**.

### Segmentation by Usage Level

- **Low usage**
- **Medium usage**
- **High usage**

### Segmentation by Age

- **Young:** under 30 years old.
- **Adult:** 30–59 years old.
- **Older Adult:** 60 years and above.

This segmentation helped identify different customer profiles and potential commercial opportunities based on their behavioral patterns.

# Key Findings

## Data Quality

- Missing values were identified in the `city` variable.
- Most missing values in `churn_date` corresponded to active customers.
- Records containing future dates from 2026 were identified as inconsistent with the project's time scope.

## Service Usage

- Most users showed a **medium level of usage**.
- Call and messaging traffic showed similar distributions between the **Basic and Premium** plans.
- Some users showed exceptionally high consumption, particularly in call minutes.

## Customer Segmentation

- The **adult** segment was the predominant age group.
- The **medium-usage** group represented the largest customer segment.
- High-usage customers represented an opportunity for premium products or specialized packages.

# Strategic Recommendations

Based on the analysis, the following recommendations were developed:

- Design commercial strategies focused on **medium-usage customers** to encourage migration to higher-tier plans.
- Create differentiated benefits for **high-usage customers**.
- Strengthen data quality controls to prevent inconsistent date records.
- Implement continuous monitoring of outliers to identify business opportunities or potential operational errors.
- Use customer segmentation to develop more targeted commercial campaigns.

# Tools Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Google Colab**
- **GitHub**

# How to Run the Project

### 1. Clone the repository
