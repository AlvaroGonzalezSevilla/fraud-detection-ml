# Detección de Fraude mediante Machine Learning

## Descripción del proyecto

Este proyecto tiene como objetivo analizar y comparar distintos modelos de *Machine Learning* para la detección de transacciones fraudulentas en conjuntos de datos financieros altamente desbalanceados.

La detección de fraude representa un problema especialmente complejo debido a que las transacciones fraudulentas constituyen un porcentaje muy pequeño frente al enorme volumen de operaciones legítimas. Por ello, se estudian diferentes enfoques de clasificación supervisada y detección de anomalías con el fin de identificar el modelo más eficaz.

---

# Metodología

El desarrollo del proyecto se ha dividido en varias etapas:

## 1. Preprocesamiento de datos

- Carga y limpieza del dataset `creditcard_limpio.csv`.
- Separación entre variables predictoras (`X`) y variable objetivo (`Class`).
- División estratificada en conjuntos de entrenamiento y prueba.
- Escalado de variables mediante `StandardScaler`.
- Aplicación de técnicas de balanceo como **SMOTE** para reducir el impacto del desbalanceo de clases.

---

## 2. Modelos implementados

Se evaluaron distintos modelos de clasificación y detección de anomalías:

### Modelos supervisados
- Regresión Logística
- Naive Bayes
- Random Forest
- HistGradientBoosting

### Modelos no supervisados / detección de anomalías
- Isolation Forest
- Local Outlier Factor (LOF)

---

## 3. Evaluación de modelos

Para medir el rendimiento de cada modelo se utilizaron las siguientes métricas:

- Accuracy
- Error Rate
- Precision
- Recall (Sensibilidad)
- Specificity
- F1 Score
- Balanced Accuracy
- Matrices de confusión

Además, se generaron:
- Curvas Precision-Recall
- Heatmaps comparativos
- Gráficas de métricas
- Comparativas globales entre modelos

---

# Aspecto clave del proyecto

En problemas de detección de fraude, la métrica más importante suele ser el **Recall**, ya que el principal objetivo es minimizar el número de fraudes no detectados (*False Negatives*).

Detectar correctamente una transacción fraudulenta es generalmente más importante que reducir ligeramente las falsas alarmas, debido al elevado coste económico asociado a los fraudes reales.

---

# Resultados obtenidos

Tras comparar todos los modelos implementados:

- **HistGradientBoosting** obtuvo el mejor equilibrio entre *Recall*, *Precision* y *F1 Score*.
- Los modelos basados en árboles mostraron un rendimiento superior frente a modelos probabilísticos simples.
- Los métodos de detección de anomalías (Isolation Forest y LOF) fueron útiles como aproximación no supervisada, aunque con menor precisión global.

---

# Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Matplotlib
- Seaborn

---

# Estructura del proyecto

- `creditcard_limpio.csv` → Dataset utilizado
- `main.ipynb / main.py` → Código principal del proyecto
- `README.md` → Documentación general
- `graficas/` → Visualizaciones y resultados obtenidos

---

# Conclusión

Este proyecto demuestra cómo diferentes técnicas de *Machine Learning* pueden aplicarse a la detección de fraude financiero, destacando la importancia del tratamiento del desbalanceo de clases y la selección adecuada de métricas de evaluación.

El análisis comparativo permitió identificar los modelos con mejor capacidad para detectar operaciones fraudulentas minimizando pérdidas potenciales.
