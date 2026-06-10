# Churn Prediction Project

## Objetivo

Desarrollar un modelo predictivo de churn utilizando técnicas de machine learning y análisis exploratorio de datos con correcta documnentacion de proyecto en un repositorio.

## Estructura del proyecto

* `data/`: base de datos original de kaggle Churn https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data.
* `notebooks/`: notebooks de preprocesamiento y modelamiento.
* `artifacts/`: datasets transformados, tablas, gráficos y modelos entrenados y varios para reporte final.

## Metodología

1. Análisis exploratorio de datos .
2. Limpieza y transformación de variables.
3. Selección de variables mediante Gini univariado.
4. Entrenamiento de modelos de regresión logística.
5. Benchmark con XGBoost.
6. Evaluación mediante AUC y Gini.

## Modelo final

Se seleccionó un modelo parsimonioso basado en 8 variables, manteniendo un desempeño similar al modelo completo.

## Tecnologías utilizadas

* Python
* Jupyter Notebook
* Scikit-Learn
* XGBoost
* Pandas
* Matplotlib
