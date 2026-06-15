# Proyecto de Predicción de Churn

## 1. Problema de Machine Learning

El objetivo del presente proyecto es desarrollar un modelo de **Machine Learning** capaz de predecir la probabilidad de abandono de clientes (**Churn**) en una empresa de telecomunicaciones.

El problema corresponde a un caso de **aprendizaje supervisado de clasificación binaria**, donde la variable objetivo es **Churn**, indicando si el cliente abandonó o permaneció en el servicio.

El propósito del modelo es identificar clientes con mayor probabilidad de fuga para facilitar estrategias de retención y toma de decisiones de negocio.

---

## 2. Diagrama de Flujo del Proyecto

Pendiente...

---

## 3. Dataset

Se utilizó un dataset de clientes de telecomunicaciones orientado a predicción de abandono de clientes (*Customer Churn*).

### Descripción del Dataset

El conjunto de datos contiene información demográfica, contractual, de consumo y facturación de clientes.

### Diccionario de Variables (resumen)

| Variable         | Descripción                       |
| ---------------- | --------------------------------- |
| gender           | Género del cliente                |
| SeniorCitizen    | Indicador de adulto mayor         |
| tenure           | Tiempo de permanencia del cliente |
| Contract         | Tipo de contrato                  |
| InternetService  | Tipo de servicio de internet      |
| PaymentMethod    | Método de pago                    |
| MonthlyCharges   | Cargo mensual                     |
| TotalCharges     | Cargo total acumulado             |
| PaperlessBilling | Facturación digital               |
| Churn            | Variable objetivo (abandono)      |

---

## 4. Estructura del Repositorio

```text
Churn/
│
├── notebooks/
│   ├── 01-preprocesamiento.ipynb
│   └── 02-Modelamiento.ipynb
│
├── data/
│   └── Dataset original
│
├── artifacts/
│   ├── modelos/
│   ├── tablas/
│   ├── graficos/
│   └── datasets procesados
│
├── README.md
├── .gitignore
└── requirements.txt
```

---

## 5. Proceso de Machine Learning

El proyecto fue desarrollado siguiendo las siguientes etapas:

### 5.1 Exploración de Datos

Se realizó un análisis exploratorio considerando:

* Tipos de variables
* Distribuciones univariadas
* Valores faltantes
* Variables categóricas y numéricas
* Detección preliminar de outliers

---

### 5.2 Calidad y Transformación de Datos

Se realizaron actividades de:

* Limpieza de datos
* Conversión de tipos de variables
* Tratamiento de variables categóricas
* Codificación ordinal basada en criterio de negocio
* Preparación de datasets para modelamiento

---

### 5.3 Selección de Variables

Se calculó el **Gini univariado** de las variables respecto al target (**Churn**) con el objetivo de identificar variables predictivas relevantes.

Posteriormente se evaluó un proceso de reducción de variables buscando un modelo más **parsimonioso**, manteniendo un desempeño competitivo con menor complejidad.

---

## 6. Modelos Utilizados

Se implementaron y compararon distintos enfoques de modelamiento:

### Regresión Logística

Se utilizó como modelo principal debido a:

* Interpretabilidad
* Simplicidad
* Facilidad de explicación del efecto de variables
* Menor complejidad operacional

Se entrenaron dos configuraciones:

* **Modelo inicial:** mayor número de variables.
* **Modelo parsimonioso:** reducción de variables buscando mantener desempeño.

### XGBoost (Benchmark)

Se implementó un modelo **XGBoost** como benchmark con el objetivo de realizar una **prueba de diferencia de algoritmo**, comparando el desempeño de un modelo lineal frente a un algoritmo basado en árboles.

Esto permitió validar la robustez del enfoque seleccionado y analizar si un modelo más complejo generaba mejoras materiales.

---

## 7. Model Card

### Objetivo del Modelo

Predecir la probabilidad de churn de clientes de telecomunicaciones.

### Tipo de Problema

Clasificación binaria.

### Variable Objetivo

* **Churn**

  * 1 = Cliente abandona
  * 0 = Cliente permanece

### Variables Utilizadas

Variables contractuales, de facturación, permanencia y servicio.

### Algoritmos Evaluados

* Regresión Logística
* XGBoost

### Consideraciones

El modelo está diseñado como ejercicio académico y no debe utilizarse directamente en producción sin monitoreo, validaciones adicionales y evaluación de sesgos.

---

## 8. Resultados

Las métricas principales utilizadas para evaluación fueron:

* **AUC (Area Under Curve)**
* **Índice de Gini**

Se realizaron comparaciones entre:

1. Modelo de Regresión Logística inicial.
2. Modelo de Regresión Logística parsimonioso.
3. Modelo XGBoost benchmark.

Se evaluó el deterioro de desempeño frente a la reducción de variables y la mejora potencial derivada del uso de algoritmos alternativos.

Los resultados mostraron que el modelo parsimonioso logró mantener un desempeño competitivo respecto al modelo inicial, reduciendo complejidad y favoreciendo interpretabilidad.

Asimismo, el benchmark con XGBoost permitió contrastar el desempeño frente a un algoritmo más complejo.

---

## 9. Artefactos Generados

El proyecto genera los siguientes artefactos:

### Modelos

* Modelo Regresión Logística (`.pkl`)
* Modelo XGBoost (`.pkl`)

### Tablas

* Gini univariado
* Selección de variables
* Comparación de modelos
* Coeficientes de regresión logística
* Importancia de variables XGBoost

### Gráficos

* Curvas ROC
* Comparación de modelos
* Importancia de variables

---

## 10. Tecnologías Utilizadas

* Python
* Pandas
* NumPy
* Scikit-Learn
* XGBoost
* Matplotlib
* Jupyter Notebook
* Git
* GitHub

---

## 11. Conclusiones

Se logró desarrollar un flujo básico de Machine Learning para predicción de churn incluyendo exploración de datos, transformación, selección de variables, entrenamiento y comparación de modelos.

El análisis permitió identificar un modelo más **parsimonioso**, capaz de mantener desempeño competitivo reduciendo complejidad e incrementando interpretabilidad.

La comparación con XGBoost permitió realizar una validación adicional del enfoque escogido mediante una prueba de diferencia de algoritmo.
