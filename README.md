**Análisis de Clientes - ConnectaTel**
**Descripción del Proyecto**

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de ConnectaTel, una empresa de telecomunicaciones en Latinoamérica, utilizando información histórica registrada hasta el año 2024.

A partir de los datos de clientes, planes y uso de servicios, se realizó un proceso de exploración, limpieza, análisis estadístico y segmentación para identificar patrones de consumo, detectar comportamientos atípicos y generar recomendaciones estratégicas para el negocio.

**Objetivos**
Evaluar la calidad de los datos disponibles.
Identificar y corregir valores nulos, sentinelas y fechas inválidas.
Analizar el comportamiento de uso de llamadas y mensajería.
Detectar valores atípicos (outliers).
Segmentar a los clientes según su nivel de uso y grupo etario.
Generar recomendaciones comerciales basadas en evidencia.
Datasets Utilizados
plans.csv

**Contiene información de los planes ofrecidos por la compañía:**

Nombre del plan
Precio mensual
Minutos incluidos
GB incluidos
Costo por excedentes
users_latam.csv

**Información demográfica y comercial de los clientes:**

Identificador de usuario
Edad
Ciudad
Fecha de registro
Tipo de plan
Fecha de cancelación (churn)
usage.csv

**Histórico de uso de los servicios:**

Identificador de usuario
Fecha de uso
Tipo de actividad (llamada o mensaje)
Duración de llamadas
Longitud de mensajes
Metodología Aplicada
1. Exploración Inicial
Carga de datasets.
Revisión de estructura.
Validación de tipos de datos.
Análisis de valores nulos.
2. Calidad de Datos

**Se identificaron:**

Valores nulos en ciudades.
Fechas de cancelación faltantes.
Valores sentinela en ciudades ("?").
Fechas futuras fuera del rango del proyecto (2026).
Valores nulos asociados al tipo de actividad registrada.
3. Limpieza de Datos

**Se realizaron las siguientes acciones:**

Conversión de fechas a formato datetime.
Reemplazo de sentinelas por valores nulos.
Corrección de fechas fuera de rango.
Conservación de nulos explicados por la naturaleza de los datos.
4. Construcción de Variables

**Se generaron indicadores por usuario:**

Cantidad de mensajes enviados.
Cantidad de llamadas realizadas.
Total de minutos consumidos.
5. Estadística Descriptiva

**Se analizaron:**

Edad.
Cantidad de mensajes.
Cantidad de llamadas.
Minutos consumidos.

**Mediante:**

Medias.
Medianas.
Cuartiles.
Histogramas.
Boxplots.
6. Segmentación de Clientes
Por nivel de uso
Bajo uso
Uso medio
Alto uso
Por edad
Joven (<30 años)
Adulto (30-59 años)
Adulto Mayor (≥60 años)
**Principales Hallazgos**
**Calidad de Datos**
Se identificaron valores faltantes en la variable ciudad.
La mayoría de los valores nulos en churn_date corresponden a clientes activos.
Se detectaron registros con fechas futuras (2026), inconsistentes con el alcance temporal del proyecto.
**Uso de Servicios**
La mayoría de usuarios presenta un nivel de uso medio.
El tráfico de llamadas y mensajes muestra distribuciones similares entre los planes Básico y Premium.
Existen usuarios con consumos excepcionalmente altos, especialmente en minutos de llamada.
**Segmentación**
Predomina el segmento de adultos.
El grupo de uso medio concentra la mayor cantidad de clientes.
Los usuarios de alto consumo representan una oportunidad para productos premium o paquetes especializados.
**Recomendaciones**
Diseñar estrategias comerciales enfocadas en usuarios de uso medio para incentivar migraciones hacia planes superiores.
Crear beneficios diferenciales para clientes de alto consumo.
Fortalecer controles de calidad para evitar registros con fechas inconsistentes.
Implementar monitoreo continuo de valores atípicos para identificar oportunidades de negocio o posibles errores operativos.
**Herramientas Utilizadas**
Python
Pandas
NumPy
Matplotlib
Seaborn
Google Colab
GitHub
**Cómo Ejecutar el Proyecto**
Clonar el repositorio:
Abrir el notebook en Google Colab o Jupyter Notebook.
Instalar dependencias:
pip install pandas numpy matplotlib seaborn
Ejecutar las celdas en orden.
Autor

Juan David Quiroz Henao
Ingeniero Ambiental | Especialista en Derecho Ambiental | Analista de Datos en formación (TripleTen)
