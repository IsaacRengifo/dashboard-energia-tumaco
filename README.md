# 🏫 Inteligencia Energética & Dashboard Multiaula - Tumaco

Dashboard web interactivo sobre el consumo energético de dos aulas (con y sin aire
acondicionado) en Tumaco. Es la versión web del cuaderno de Google Colab
`ejercicio_final.py`, con los datos reales del dataset y las mismas métricas y gráficos.

## Contenido

| Pestaña | Qué muestra |
|---|---|
| Análisis Exploratorio (EDA) | Tabla de datos, estadísticas descriptivas, histograma de potencia, temperatura vs potencia y matriz de correlación |
| Comparativa Energética | Energía total, potencia promedio/máx/mín, consumo diario, ocupado/vacío y anomalías por aula |
| Regresión (Predicción) | Métricas del MLP (MAE, MSE, RMSE, R², MAPE, sesgo, curtosis) e histograma de residuos |
| Clasificación & Diagnóstico | Accuracy, precision/recall, curva ROC y matriz de confusión del consumo inusual |
| Clustering | Segmentación K-Means en 3 clústeres |
| Series Temporales | Consumo real vs. predicción LSTM y GRU |
| Simulador IoT | Estimación interactiva de consumo según temperatura, ocupación y tipo de aula |
| Conclusiones & Recomendaciones | Hallazgos basados en los resultados |

## Características

- **Un solo archivo**: `index.html` incluye los datos (JSON) y Plotly incrustados.
  No necesita servidor, base de datos ni conexión a internet.
- **100 % estático**: ideal para Vercel, GitHub Pages o cualquier hosting de archivos.
- **Interactivo**: pestañas, selector de visualizaciones, tooltips de Plotly y simulador.

## Resultados principales

- Energía total: 222,20 kWh (aula con AC) vs. 66,34 kWh (aula sin AC).
- Regresión MLP: R² = 0,8965 · MAE = 0,02169 kWh · RMSE = 0,02925 kWh.
- Clasificación de consumo inusual: accuracy = 1,0000 · AUC = 1,0000.
- Dataset: 5.760 registros, 18 variables, del 01/09/2026 al 30/09/2026.

## Despliegue

El proyecto está listo para Vercel: no requiere build.

- Framework Preset: **Other**
- Build Command: *(vacío)*
- Output Directory: *(vacía)*

## Tecnologías

Python (pandas, scikit-learn, TensorFlow/Keras, Plotly) para el análisis y la generación
de figuras; HTML + CSS + JavaScript + Plotly.js para la página final.
