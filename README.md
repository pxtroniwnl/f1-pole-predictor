# 🏎️ F1 Pole Predictor: Suzuka 2026 Edition
### Machine Learning & Telemetry Analysis for Pole Position Prediction

Este proyecto aplica técnicas avanzadas de **Ciencia de Datos** y **Machine Learning** para predecir la parrilla de salida del Gran Premio de Japón 2026. Utiliza un enfoque híbrido que combina la precisión de la telemetría histórica con el estado de forma actual de la temporada.

![F1 Data Science](https://img.shields.io/badge/Domain-Data%20Science-red?style=flat-square&logo=formula1)
![Python](https://img.shields.io/badge/Python-3.12-blue?style=flat-square&logo=python)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange?style=flat-square)

## 📊 Descripción del Proyecto
El objetivo principal es predecir el **Gap to Pole** (diferencial de tiempo en segundos respecto al primer lugar). El sistema se basa en dos pilares:

1.  **Modelo A (Telemetría Histórica - XGBoost):** Entrenado con datos de los GPs de Japón 2022, 2023 y 2024. Analiza sectores (S1, S2, S3), `AvgSpeed`, y `ThrottleFullPct` para entender qué coche se adapta mejor a la carga aerodinámica de Suzuka.
2.  **Modelo B (Estado de Forma 2026):** Un análisis de momentum que promedia los resultados de clasificación de las rondas previas de 2026 (Bahréin, Arabia Saudita y Australia).

## 🛠️ Stack Tecnológico
* **Librerías Core:** `FastF1`, `XGBoost`, `Scikit-Learn`.
* **Procesamiento:** `Pandas`, `Numpy`.
* **Visualización:** `Matplotlib`, `Seaborn`.

## 📈 Resultados y Optimización
Tras realizar un `GridSearchCV` para optimizar hiperparámetros, el modelo alcanzó un **MAE (Error Absoluto Medio) de 155.10 ms**, lo que permite una precisión competitiva dentro de la misma décima de segundo.

**Variables Críticas identificadas:**
* **AvgSpeed:** Factor determinante por el flujo constante del circuito.
* **S1_ms:** Las eses de Suzuka definen la ventaja competitiva del chasis.

## 🚀 Instalación y Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/pxtroniwnl/f1-pole-predictor.git](https://github.com/pxtroniwnl/f1-pole-predictor.git)
   cd f1-pole-predictor
