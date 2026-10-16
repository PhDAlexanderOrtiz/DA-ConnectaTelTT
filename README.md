📊 Análisis Exploratorio de Datos y Comportamiento del Cliente - ConnectaTel

📝 Descripción del Proyecto

Este proyecto de analítica de datos aborda el estudio de los patrones de consumo de voz y mensajería, la utilización de servicios telefónicos y la retención de clientes en la compañía de telecomunicaciones ConnectaTel.

Como analistas de datos, evaluamos exclusivamente el nivel de uso real de las líneas telefónicas en términos de llamadas (minutos) y mensajes de texto (SMS) en relación con los límites fijados en los planes Básico y Premium. El objetivo es identificar oportunidades estratégicas para optimizar la oferta comercial de telefonía, reducir la tasa de cancelación (churn) y mejorar la satisfacción global del usuario.

Nota del Alcance: Este estudio se centra de forma exclusiva en el consumo de minutos de voz y SMS. No se incluyen ni analizan servicios de internet móvil o consumo de datos.

🎯 Objetivos

Objetivo Principal: Analizar el comportamiento de uso telefónico de los clientes para identificar patrones de consumo de voz/SMS y brechas respecto a la oferta de los planes vigentes.

Objetivos Específicos:

Cuantificar el consumo promedio mensual de llamadas (número y duración en minutos) y mensajes de texto (SMS) por segmento de cliente.

Determinar la brecha de subutilización entre los límites de voz y SMS contratados frente al consumo real en los planes Básico y Premium.

Formular recomendaciones accionables de negocio para el diseño de planes de telefonía más ajustados, estrategias de retención y propuestas de valor en el segmento Premium.

💾 Datasets Utilizados

El análisis combina y procesa conjuntos de datos estructurados enfocados en usuarios, planes tarifarios y uso de voz/SMS:

Usuarios (users): Información demográfica y contractual de los clientes (ID de usuario, ciudad, fecha de alta/baja y plan contratado).

Planes (plans): Estructura tarifaria y cuotas asignadas de minutos y SMS para los planes Básico y Premium.

Registro de Uso (usage / calls / messages): Registros detallados por usuario del número de llamadas realizadas, minutos consumidos y cantidad de mensajes de texto enviados por mes.

🛠️ Etapas del Análisis

El desarrollo del proyecto siguió un flujo riguroso de analítica de datos compuesto por las siguientes fases:

Limpieza y Preparación de Datos (Data Wrangling):

Imputación y gestión de valores nulos (p. ej., fechas de baja en usuarios activos).

Conversión y estandarización de tipos de datos (fechas y variables cuantitativas).

Verificación y tratamiento de registros con duraciones de llamadas o mensajes.

Ingeniería de Características y Agregación:

Consolidación mensual por usuario del total de llamadas, minutos hablados y mensajes enviados.

Cálculo del porcentaje de consumo efectivo de voz y SMS frente a las cuotas máximas de cada plan.

Análisis Exploratorio de Datos (EDA) y Estadística Descriptiva:

Cálculo de medidas de tendencia central (media, mediana) y dispersión para minutos y SMS.

Comparación de consumo entre los usuarios del plan Básico (~64.9%) y el plan Premium (~35.1%).

Identificación de Hallazgos y Patrones Clave:

Subutilización de Servicios Telefónicos: Los usuarios consumen en promedio una fracción mínima de sus límites (~4.5 llamadas, ~23.3 minutos y ~5.5 SMS al mes), muy por debajo de las capacidades contratadas (100 a 600 minutos y 100 a 500 SMS).

Comportamiento en Segmento Premium: Los usuarios Premium tampoco saturan los límites de minutos ni SMS, lo que indica que incrementar cuotas de voz/mensajería tradicional no añade valor percibido.

Señales de Churn: Reducción drástica en la frecuencia de llamadas y SMS como indicador previo al abandono del servicio.

Recomendaciones Estratégicas:

Rediseño de planes de telefonía hacia esquemas más flexibles o modulares y alertas tempranas de baja actividad telefónica.

🚀 Cómo Ejecutar el Notebook

Opción 1: Google Colab (Recomendado)

Abre Google Colab.

Ve a Archivo > Subir notebook y selecciona el archivo .ipynb de este repositorio.

Carga los archivos .csv correspondientes en el almacenamiento temporal de la sesión.

Ejecuta las celdas en orden secuencial (Shift + Enter o Entorno de ejecución > Ejecutar todas).

Opción 2: Entorno Local (Jupyter Notebook)

Clona este repositorio:

git clone https://github.com/tu-usuario/connectatel-data-analysis.git
cd connectatel-data-analysis


Crea e activa un entorno virtual e instala las dependencias:

python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
pip install pandas numpy matplotlib seaborn jupyter


Inicia Jupyter Notebook y abre el cuaderno de trabajo:

jupyter notebook


📋 Guía de Reproducción

Carga de Datos: Verifica la correcta ubicación de los archivos CSV de usuarios, planes y registros de uso.

Entorno: Asegúrate de contar con pandas, numpy, matplotlib y seaborn instalados.

Ejecución: Corre los bloques de código de forma secuencial, desde la limpieza e integración de datos hasta las celdas de agregación y visualización gráfica.

✒️ Autores y Créditos

Proyecto desarrollado por el equipo de Analítica de Datos para el análisis de comportamiento de clientes en ConnectaTel.
