# Predicción de Churn de Clientes (Telco)

Proyecto de ciencia de datos de extremo a extremo: predicción de cancelación de clientes
(*customer churn*) para una empresa de telecomunicaciones, usando datos reales de 7,043
clientes.

## Contexto del problema

Retener un cliente existente cuesta significativamente menos que adquirir uno nuevo.
Este proyecto construye un modelo que identifica, a partir del perfil y los servicios
contratados de un cliente, su probabilidad de cancelar — permitiendo a una empresa
anticipar acciones de retención.

## Qué incluye este repo

- **`notebooks/01_eda_baseline.ipynb`**: análisis exploratorio completo (limpieza de
  datos, distribución de la variable objetivo, relación entre variables clave y churn)
  y un modelo baseline de clasificación (Regresión Logística) con evaluación honesta
  (precision, recall, F1, ROC-AUC — no solo accuracy, que es engañoso en problemas
  desbalanceados).
- **`data/`**: dataset original (IBM Telco Customer Churn, de uso público).

## Hallazgos principales

- ~26.5% de tasa de churn general.
- Los contratos mes a mes concentran una tasa de cancelación mucho mayor que los
  contratos anuales — el compromiso contractual retiene.
- La mayoría de las cancelaciones ocurre en los primeros meses de vida del cliente.
- Cargos mensuales más altos se asocian a mayor cancelación.

## Cómo correrlo

```bash
pip install -r requirements.txt
jupyter notebook notebooks/01_eda_baseline.ipynb
```

## Próximos pasos

- [ ] Comparar modelos (Random Forest, Gradient Boosting) contra el baseline.
- [ ] Interpretabilidad con SHAP para explicar predicciones por cliente individual.
- [ ] Ajuste del umbral de decisión según costo de negocio real.
- [ ] Dashboard interactivo en Streamlit.

## Stack

Python · pandas · scikit-learn · matplotlib · seaborn

---
*Dataset: [IBM Telco Customer Churn](https://github.com/IBM/telco-customer-churn-on-icp4d), de uso público y educativo.*
