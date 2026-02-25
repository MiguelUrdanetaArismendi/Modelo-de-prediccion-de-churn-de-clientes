# Predicción de Churn de Clientes — Telecom Dataset

## Descripción del proyecto

El objetivo de este proyecto es desarrollar un modelo predictivo capaz de identificar clientes con riesgo de abandono (**churn**) en una empresa de telecomunicaciones.

La retención de clientes es uno de los principales retos del sector, por lo que disponer de modelos que permitan anticipar el abandono permite optimizar campañas de fidelización y reducir pérdidas de ingresos.

El proyecto cubre el flujo completo de un caso real de Data Science:
- Limpieza y transformación de datos
- Análisis exploratorio (EDA)
- Feature Engineering
- Modelado predictivo
- Evaluación del modelo

---

## Dataset

Se utiliza el dataset público **Telco Customer Churn** (Kaggle), que contiene información demográfica, contractual y de servicios de 7043 clientes.

Variables relevantes:
- Tipo de contrato
- Servicios contratados
- Cargos mensuales y totales
- Antigüedad del cliente
- Variable objetivo: **Churn**

---

## Estructura del proyecto

├── data
│ ├── raw
│ └── processed
├── notebooks
│ ├── 01_eda_cleaning.ipynb
│ ├── 02_feature_engineering.ipynb
│ └── 03_modeling.ipynb
└── README.md

---

## Proceso

### 1. Data Cleaning
- Conversión de tipos de datos
- Tratamiento de valores faltantes
- Eliminación de variables no predictivas

### 2. Ánalisis exploratorio (EDA)
- Comparación de variables númericas
- Comparación de variables categóricas

### 3. Feature Engineering
- Encoding de variables categóricas
- Escalado de variables numéricas
- Preparación de dataset para modelado
- Train/Test split (80/20)

### 4. Modelado
Se implementó un modelo baseline utilizando:

**Logistic Regression**

Se realizó:
- Escalado con StandardScaler
- Evaluación con métricas de clasificación

---

## Resultados

Métricas principales:

- Accuracy: **0.80**
- F1-score (Churn): **0.61**
- Recall (Churn): **0.57**

El modelo demuestra capacidad para detectar patrones de abandono, constituyendo un baseline válido para futuras mejoras mediante modelos más complejos.

---

## Conclusiones clave

- Los contratos **month-to-month** presentan mayor churn.
- Clientes con mayor **Cargos mensuales (MonthlyCharges)** tienden a abandonar más.
- Los clientes con menor **antigüedad (tenure)** tienen mayor probabilidad de churn.
- La ausencia de servicios adicionales está asociada a mayor abandono.

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib / Seaborn
- Jupyter Notebook
