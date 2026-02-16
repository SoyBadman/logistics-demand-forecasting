🚖 Pronóstico de Demanda Logística - Series Temporales

📖 Descripción del Proyecto

Una empresa de transporte necesita optimizar la asignación de sus flotas para satisfacer la demanda de usuarios en horas pico. Si no hay suficientes vehículos, se pierden clientes; si hay demasiados, se pierden recursos.

El objetivo de este proyecto es desarrollar un modelo de Machine Learning capaz de pronosticar la cantidad de pedidos de transporte para la próxima hora, basándose en datos históricos de series temporales.

🎯 Objetivo de Negocio

Problema: Ineficiencia en la distribución de vehículos durante cambios bruscos de demanda.

Meta: Construir un modelo predictivo con un margen de error (RMSE) inferior a 48 pedidos.

Impacto: Maximizar la disponibilidad del servicio en horas pico y reducir costos operativos en horas valle.

🛠️ Tecnologías y Herramientas

Lenguaje: Python 3.9+

Librerías: Pandas, NumPy, Statsmodels, Matplotlib.

Machine Learning: Scikit-learn (Regresión Lineal, Random Forest), LightGBM/CatBoost.

Métrica de Evaluación: RMSE (Raíz del Error Cuadrático Medio).

⚙️ Metodología del Proyecto

Análisis y Procesamiento de Datos (Time Series Analysis):

Remuestreo de datos (Resampling) a intervalos de 1 hora.

Análisis de tendencias y estacionalidad utilizando seasonal_decompose.

Verificación de estacionariedad para asegurar la validez de las predicciones.

Ingeniería de Características (Feature Engineering):

Creación de Desfases (Lags): Para capturar la influencia de horas pasadas en el presente.

Medias Móviles (Rolling Mean): Para suavizar la tendencia y capturar el comportamiento general.

Extracción de características temporales (hora del día, día de la semana).

Modelado y Evaluación:

División de datos respetando la secuencia temporal (Train/Test split sin shuffling).

Entrenamiento de modelos de regresión y prueba de sanidad (Sanity Check).

Optimización de hiperparámetros.

📊 Resultados

El modelo final seleccionado logró superar el KPI establecido por la empresa:

Métrica

Resultado Obtenido

Meta del Proyecto

RMSE (Test)

43.59

< 48.0

Esto significa que el modelo tiene un error promedio de solo ~43 pedidos por hora, permitiendo una planificación operativa eficiente.

