# **Análisis de Cancelación de Clientes (Churn Prediction)**

## **Descripción del Proyecto**

Este proyecto tiene como objetivo **predecir la cancelación de clientes** (Churn) en una empresa de telecomunicaciones. Utilizando un conjunto de datos de clientes, se entrenaron y evaluaron varios modelos de clasificación para identificar los principales factores que influyen en la cancelación. Los modelos utilizados incluyen **Regresión Logística**, **Random Forest**, y **VotingClassifier** (ensemble), cada uno con un análisis de **importancia de variables** para ayudar en la toma de decisiones estratégicas.

## **Objetivos del Proyecto**

- **Preprocesamiento de datos**: Limpieza y codificación de variables categóricas, manejo de valores nulos y normalización.
- **Entrenamiento de Modelos**: Implementación de modelos de **Regresión Logística**, **Random Forest**, y **VotingClassifier** para predecir la cancelación de clientes.
- **Evaluación de Modelos**: Análisis de métricas como **precisión**, **recall**, **AUC-ROC** y **F1-score** para comparar el rendimiento de los modelos.
- **Análisis de Variables Importantes**: Identificación de las variables clave que influyen en la cancelación de clientes.
- **Propuesta de Estrategias de Retención**: Basado en los resultados, se sugieren estrategias para reducir la tasa de cancelación.

## **Estructura del Proyecto**

1. **Preprocesamiento de Datos**:
   - Carga y limpieza de datos.
   - Aplicación de **One-Hot Encoding** en variables categóricas.
   - Normalización de datos para modelos sensibles a la escala (Regresión Logística y KNN).

2. **Modelos de Predicción**:
   - **Regresión Logística**: Utilizada para predecir la probabilidad de cancelación con base en los coeficientes de cada variable.
   - **Random Forest**: Modelo basado en árboles que calcula la importancia de las variables mediante la reducción de la impureza en las divisiones de los árboles.
   - **VotingClassifier**: Combinación de **Regresión Logística** y **Random Forest** utilizando una votación ponderada (soft voting).

3. **Evaluación de Modelos**:
   - Comparación de los modelos usando **classification_report**, **confusion_matrix**, **roc_auc_score**.

4. **Análisis de Variables**:
   - Identificación de las variables más relevantes para la predicción de la cancelación usando los coeficientes de **Regresión Logística** y la **importancia de características** de **Random Forest**.

## **Métricas Utilizadas**

- **Exactitud (Accuracy)**: Proporción de predicciones correctas.
- **Precisión**: Proporción de verdaderos positivos sobre los positivos predichos.
- **Recall**: Proporción de verdaderos positivos sobre los casos reales positivos.
- **F1-Score**: Promedio armonizado entre precisión y recall.
- **AUC-ROC**: Capacidad del modelo para discriminar entre las clases.

## **Resultados Principales**

- **Mejor desempeño**: El modelo **Regresión Logística** mostró el mejor **AUC-ROC** (0.84) y **recall** (0.91) para los **clientes cancelados**.
- **Random Forest** y **VotingClassifier** también tuvieron un buen desempeño, aunque con un **AUC-ROC** ligeramente inferior.
- **Variables clave**: Las principales variables que influyen en la cancelación son **gasto total**, **tiempo de contrato** (uno o dos años) y **tipo de servicio de Internet** (fibra óptica).

## **Estrategias de Retención Propuestas**

1. **Fidelización de clientes con contratos largos**: Ofrecer incentivos para clientes con contratos de **dos años**.
2. **Revisión de precios**: Considerar **descuentos personalizados** para clientes con **altos gastos mensuales**.
3. **Mejorar la calidad del servicio de fibra óptica**: Los clientes con este servicio muestran una mayor tasa de cancelación.
4. **Opciones de pago**: Facilitar métodos de pago más automáticos y fáciles para reducir la cancelación asociada a **cheques electrónicos**.

## **Requisitos**

- **Python 3.x**
- **Librerías**:
  - `pandas`
  - `numpy`
  - `scikit-learn`
  - `xgboost`
  - `matplotlib`
  - `seaborn`



## **Archivos**

- **`DatosTratados.csv`**: El conjunto de datos utilizado para entrenar y evaluar los modelos.
- **`TelecomX_parte_2.ipynb`**: Script de ejecución.

