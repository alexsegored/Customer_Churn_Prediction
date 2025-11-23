# 🧩 Customer Churn Prediction
---
[![Python](https://img.shields.io/badge/Python-3.15-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)](https://jupyter.org/)
---

## 📋 Descripción del Proyecto

Proyecto de predicción de churn (abandono de clientes) en el sector de telecomunicaciones mediante técnicas de Machine Learning.

### Objetivo
Este proyecto analiza datos de clientes de telecomunicaciones para desarrollar un modelo predictivo que identifique patrones asociados al abandono del servicio. El proceso incluye exploración de datos, preprocesamiento, entrenamiento de modelos y evaluación de resultados.

### Dataset
Se utiliza el dataset "Telco Customer Churn" que incluye información sobre:

- Características demográficas de los clientes
- Servicios contratados
- Información de facturación
- Estado de permanencia del cliente (variable objetivo)

### Metodología

1. **Análisis Exploratorio (EDA)**: Visualización y análisis estadístico para comprender la distribución de variables y relaciones entre características.
2. **Preprocesamiento**: Tratamiento de valores faltantes, codificación de variables categóricas y transformación de features.
3. **Modelado y Evaluación**: Entrenamiento de algoritmos de clasificación, optimización de hiperparámetros y evaluación mediante métricas de rendimiento.

## 📁​ Estructura del proyecto
```
Customer_Churn_Prediction/
│
├── 💾​ data/
│   ├── processed/               # Datos procesados
│   └── Telco-Customer-Churn.csv # Datos originales
│
├── 📓​ notebooks/
│   ├── EDA.ipynb                # Análisis exploratorio
│   ├── ModelTraining.ipynb      # Logistic Regression XGBoost Random Forest
│   └── Preprocessing.ipynb      # Preprocesamiento
│
├── .gitattributes
├── .gitignore
├── 📖​ README.md
└── ​📄​ requirements.txt
```

## 🚀 Cómo Usar
1. Clona el repositorio:
```
git clone https://github.com/alexsegored/Customer_Churn_Prediction.git
```
2. Instala las dependencias
```
pip install -r requirements.txt
```
3. Ejecuta los notebooks en orden
- Primero: `EDA.ipynb`
- Segundo: `Preprocessing.ipynb`
- Tercero: `ModelTraining.ipynb`

## 📊 Resultados

### Modelo Final
Se utilizó **Regresión Logística** como modelo final, con un threshold optimizado de **0.45** basado en el F1-score.

### Métricas de Rendimiento

| Métrica | Clase 0 (No Churn) | Clase 1 (Churn) |
|---------|-------------------|-----------------|
| **Precision** | 0.866 | 0.607 |
| **Recall** | 0.851 | 0.636 |
| **F1-Score** | 0.858 | 0.621 |

- **Accuracy general**: 79.4%
- **Macro avg F1-Score**: 0.740
- **Weighted avg F1-Score**: 0.795

### Matriz de Confusión

|  | Predicho: No Churn | Predicho: Churn |
|---|---|---|
| **Real: No Churn** | 879 | 154 |
| **Real: Churn** | 136 | 238 |

### Variables Más Importantes

Las siguientes características muestran la **importancia absoluta** de los coeficientes del modelo:

**Servicios contratados:**
- InternetService_Fiber optic (~2.1)
- StreamingTV_Yes (~0.9)
- StreamingMovies_Yes (~0.8)
- MultipleLines_Yes (~0.6)

**Información financiera:**
- MonthlyCharges (~1.8)
- TotalCharges (~0.7)
- PaymentMethod_Electronic check (~0.4)

**Características del contrato:**
- Contract_Two year (~1.5)
- Contract_One year (~0.75)
- Tenure (~1.5)

## 🤝 Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un issue o pull request para sugerencias o mejoras.