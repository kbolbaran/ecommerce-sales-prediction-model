# 📈 Forecasting de Ventas con Prophet + Eventos Especiales

Este proyecto utiliza **Facebook Prophet** para predecir los montos diarios de venta del eCommerce, incorporando eventos especiales como **CyberDays**, **Black Friday** y campañas comerciales específicas.

## 🧠 Modelo utilizado

Se entrenó un modelo Prophet optimizado con los siguientes parámetros:

- `changepoint_prior_scale`: `0.01`
- `seasonality_prior_scale`: `0.01`
- `holidays_prior_scale`: `1.0`
- `seasonality_mode`: `multiplicative`

Además, se incluyeron **festividades personalizadas** como variables externas (`holidays`) para mejorar la precisión del modelo.

## 📊 Métricas de evaluación

Después de ajustar el modelo y evaluar con datos de validación:

- **MAPE**: `2.98%`
- **MAE**: `0.49`
- **MSE**: `0.40`

Estas métricas indican una alta precisión del modelo al predecir montos de ventas diarias.

## 📅 Eventos personalizados incluidos

- `cyber_days_mayo`
- `cyber_days_octubre`
- `black_friday`
- `evento_especial` 

Cada evento fue separado y registrado con su propio nombre en la variable `holidays`, lo que permite a Prophet capturar su impacto estacional.

## 📦 Archivos involucrados

- `Curva_entrenamiento.xlsx`: archivo base con ventas históricas.
- `Proyeccion_ganancias_v2.ipynb`: modelo Prophet.
- `Prediccion_montos_v2`: predicciones exportadas para análisis o visualización.

## 🚀 Cómo usar

1. Asegúrate de tener Python y las librerías necesarias (`prophet`, `pandas`, `matplotlib`, etc.).
2. Ejecuta el script para entrenar el modelo y generar el archivo con predicciones.
3. Evalúa el rendimiento del modelo con las métricas incluidas.


---



