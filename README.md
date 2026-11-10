# 📊 Análisis de Comportamiento de Clientes y Planes Telefónicos — ConnectaTel

> *Contexto formativo: Este proyecto forma parte de la ruta de especialización en Data Analysis de TripleTen.*

---

## 1. Resumen Ejecutivo (BLUF)
* **Impacto Directivo:** El análisis exploratorio y estadístico de los datos de **ConnectaTel** revela una masiva brecha de subutilización: los clientes consumen en promedio una fracción menor a los límites contratados (~4.5 llamadas, ~23.3 minutos y ~5.5 mensajes al mes).
* **Decisión Estratégica:** La gran mayoría de los usuarios se concentran en el plan *Básico*, pero incluso este plan excede las necesidades reales de consumo. Se recomienda rediseñar la estructura tarifaria y enfocar campañas de retención en clientes con caídas drásticas de actividad (*churn*).

---

## 2. Estructura y Datos del Proyecto
* **Origen de los Datos:** Datasets estructurados de clientes, llamadas, mensajes y configuración de planes de ConnectaTel.
* **Datasets Utilizados:**
  1. **`users.csv` / `users.json`**: Información demográfica, ciudad, fecha de alta, plan y fecha de baja (*churn*).
  2. **`calls.csv`**: Registro de llamadas (ID, usuario, fecha y duración en minutos).
  3. **`messages.csv`**: Registro de mensajes de texto (ID, usuario y fecha de envío).
  4. **`plans.csv`**: Tarifas y límites (*Básico*: 12 USD, 100 min, 100 SMS | *Premium*: 25 USD, 600 min, 500 SMS).
* **Nota de Alcance:** Análisis enfocado exclusivamente en llamadas y mensajes de texto (SMS); no incluye datos ni variables de internet o datos móviles.
* **Reproducibilidad:** Acceso mediante [Google Colab](https://colab.research.google.com/) y ejecución local vía clonación de repositorio.

---

## 3. Metodología y Enfoque Analítico
* **Librerías y Herramientas:** `pandas`, `numpy`, `matplotlib`, `seaborn` en entornos Jupyter Notebook / Google Colab.
* **Limpieza y Preparación:** 
  * Tratamiento de valores nulos y duplicados.
  * Corrección de valores atípicos y *sentinels* (como `-999` en edad y `?` en ciudades).
  * Estandarización de tipos de datos y fechas.
* **Análisis Exploratorio y Estadístico:**
  * Agregación mensual de consumo por usuario.
  * Cálculo de métricas descriptivas (media, mediana, desviación estándar, percentiles).
  * Detección de outliers mediante diagramas de caja (*boxplots* optimizados con `showmeans=True`).
  * Segmentación de clientes cruzando variables demográficas y de uso.

---

## 4. Descubrimientos y Hallazgos Principales (Core)
* **Brecha de Subutilización Extrema:** El consumo mensual por cliente es drásticamente inferior a las cuotas incluidas en los planes, evidenciando sobre-aprovisionamiento en los paquetes actuales.
* **Concentración en Plan Básico:** La base de usuarios está mayoritariamente en el plan de menor costo, donde persiste la subutilización.
* **Patrón de Cancelación (*Churn*):** Los clientes que presentan reducciones drásticas y repentinas en su volumen de llamadas y mensajes de texto muestran una propensión marcadamente mayor a cancelar el servicio.

---

## 5. Limitaciones Metodológicas
* **Exclusión de Tráfico de Datos:** El alcance se limita estrictamente a voz y SMS, dejando fuera métricas de consumo de internet móvil.
* **Ventana Temporal:** Los datos provienen de un periodo de observación específico, por lo que estacionalidades de largo plazo o cambios macroeconómicos no están modelados.
* **Supuestos de Imputación:** La imputación de valores faltantes y demográficos asume distribuciones normales o paramétricas estándar (*MAR*).

---

## 6. Próximos Pasos Estratégicos
* **Rediseño Tarifario:** Introducir planes flexibles o micro-paquetes para capturar a los usuarios con consumo bajo que hoy perciben el plan Básico como costoso.
* **Sistema de Alerta Temprana de Churn:** Implementar un modelo predictivo basado en la caída de llamadas/SMS para activar protocolos de retención a tiempo.
* **Optimización de Canales de Soporte:** Fortalecer el acompañamiento a clientes en zonas con mayor tasa de deserción.

---

## 🚀 Cómo Ejecutar el Notebook

### Opción 1: Abrir directamente en Google Colab (Recomendado)
1. Haz clic en o abre [Google Colab](https://colab.research.google.com/).
2. Selecciona la pestaña **GitHub**.
3. Pega la URL de este repositorio y selecciona el archivo `.ipynb`.
4. Ejecuta las celdas secuencialmente presionando `Shift + Enter`.

### Opción 2: Ejecución Local en Jupyter Notebook / VS Code
1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/nombre-del-repositorio.git](https://github.com/tu-usuario/nombre-del-repositorio.git)
   cd nombre-del-repositorio
