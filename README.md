# 📊 Análisis de Comportamiento de Clientes y Planes Telefónicos — ConnectaTel

Este repositorio contiene el análisis exploratorio y estadístico realizado para la empresa de telecomunicaciones **ConnectaTel**. El objetivo principal como analistas de datos fue evaluar el comportamiento de uso de los clientes respecto a las llamadas y mensajes de texto en sus respectivos planes contratados, identificar brechas de subutilización y proponer recomendaciones estratégicas orientadas a la optimización de la oferta comercial y la retención de clientes.

---

## 🎯 Objetivo del Proyecto

* **Analizar el uso real** de servicios de telefonía (minutos de llamada y mensajes de texto) por parte de los clientes.
* **Evaluar la adecuación** de los planes actuales (*Básico* y *Premium*) según los patrones de consumo identificados.
* **Identificar factores y patrones** asociados a la baja de clientes (*churn*).
* **Formular recomendaciones basadas en datos** para optimizar la estructura tarifaria, reducir la deserción y mejorar la satisfacción del cliente.

---

## 📁 Datasets Utilizados

El análisis se fundamenta en los siguientes conjuntos de datos estructurados:

1. **`users.csv` / `users.json`**: Información demográfica y de cuenta de los clientes (ID de usuario, nombre, ciudad, fecha de alta, plan contratado y fecha de baja/churn si aplica).
2. **`calls.csv`**: Registro de llamadas realizadas (ID de llamada, ID de usuario, fecha y duración en minutos).
3. **`messages.csv`**: Registro de mensajes de texto enviados (ID de mensaje, ID de usuario y fecha de envío).
4. **`plans.csv`**: Configuración de las tarifas y límites de cada plan:
   * **Plan Básico**: 12 USD/mes | 100 minutos de llamadas | 100 mensajes de texto.
   * **Plan Premium**: 25 USD/mes | 600 minutos de llamadas | 500 mensajes de texto.

> **Nota de Alcance:** El análisis se enfoca de manera exclusiva en minutos de voz y mensajes de texto (SMS). No se incluyen datos ni variables referentes al uso de internet o datos móviles.

---

## 🛠️ Etapas del Análisis Realizado

1. **Carga y Preparación de Datos:**
   * Importación de librerías esenciales (`pandas`, `numpy`, `matplotlib`, `seaborn`).
   * Limpieza de datos: tratamiento de valores nulos, verificación de duplicados y conversión de tipos de datos (fechas y numéricos).

2. **Análisis Exploratorio de Datos (EDA):**
   * Agregación mensual del consumo por usuario (total de llamadas, minutos consumidos y mensajes enviados).
   * Cálculo de métricas estadísticas clave (media, mediana, desviación estándar, percentiles).
   * Visualización de distribuciones de consumo mediante histogramas y diagramas de caja (*boxplots*).

3. **Evaluación de Subutilización de Servicios:**
   * Comparación cuantitativa entre las cuotas incluidas en los planes y el consumo real promedio de los clientes.
   * Identificación del porcentaje de usuarios que saturan o sobrepasan sus límites contratados.

4. **Análisis de Cancelación de Clientes (*Churn*):**
   * Evaluación de la tasa de retención frente a la fecha de cancelación.
   * Correlación entre la inactividad/bajo volumen de llamadas/SMS y la probabilidad de baja.

5. **Conclusiones y Recomendaciones Estratégicas:**
   * Formulación de propuestas operativas y comerciales respaldadas por la evidencia analítica.

---

## 💡 Hallazgos Clave

* **Brecha de Subutilización:** El consumo promedio mensual por cliente es drásticamente inferior a los límites que ofrecen los planes (promedio ~4.5 llamadas, ~23.3 minutos y ~5.5 mensajes al mes).
* **Distribución de Clientes:** La mayoría de los usuarios están concentrados en el plan *Básico*, sin embargo, incluso en este nivel la capacidad incluida sobrepasa con frecuencia sus necesidades reales.
* **Patrón de Deserción:** Los clientes con drástica reducción en su actividad de llamadas y mensajes presentan una mayor propensión a cancelar el servicio.

---

## 🚀 Cómo Ejecutar el Notebook

### Opción 1: Abrir directamente en Google Colab (Recomendado)

1. Haz clic en el siguiente enlace o abre [Google Colab](https://colab.research.google.com/).
2. Selecciona la pestaña **GitHub**.
3. Pega la URL de este repositorio y selecciona el archivo `.ipynb`.
4. Ejecuta las celdas secuencialmente presionando `Shift + Enter`.

### Opción 2: Ejecución Local en Jupyter Notebook / VS Code

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/nombre-del-repositorio.git](https://github.com/tu-usuario/nombre-del-repositorio.git)
   cd nombre-del-repositorio
