# Proyecto de Predicción de Ingresos de Adultos

## Descripción del Proyecto

Este proyecto analiza el conocido **Adult Income Dataset**, el cual predice si los ingresos de un individuo superan los $50K/año en función de diversos factores demográficos y personales. Este dataset es un excelente punto de partida para prácticas de preprocesamiento de datos y aprendizaje automático.

---

## Descripción del Dataset

- **Fuente**: El dataset contiene 16 columnas con 14 atributos que describen características demográficas y otras cualidades de los individuos.
- **Variable Objetivo**: `Income` (clasificación binaria: `<=50K` y `>50K`).
- **Atributos**:
  - `age`, `workclass`, `fnlwgt`, `education`, `educational-num`, `marital-status`, `occupation`, `relationship`, `race`, `gender`, `capital-gain`, `capital-loss`, `hours-per-week`, `native-country`.

---

## Principales Pasos en el Proyecto

1. **Carga de Datos**:
   - Lectura del dataset utilizando `pandas` y exploración de su estructura inicial.

2. **Análisis Exploratorio de Datos (EDA)**:
   - Análisis de distribuciones usando `.value_counts()` para características como `education`, `occupation`, `workclass` y `gender`.
   - Visualización de correlaciones entre las características mediante un mapa de calor.

3. **Preprocesamiento de Datos**:
   - Transformación de variables categóricas mediante codificación one-hot para columnas como `occupation`, `workclass`, `marital-status`, `relationship`, `race` y `native-country`.
   - Binarización de `gender` (`Male` = 1, `Female` = 0) y `income` (`>50K` = 1, `<=50K` = 0).
   - Eliminación de columnas irrelevantes o con baja significancia basándose en el análisis de correlaciones.

4. **Ingeniería de Características**:
   - Retención de las columnas más significativas según un umbral de correlación para simplificar el modelo.

5. **Visualización**:
   - Mapa de calor para ilustrar las correlaciones entre características y la variable objetivo (`income`).

---

## Tecnologías y Librerías Clave

- **Lenguajes**: Python
- **Librerías**:
  - `pandas`: Manipulación y preprocesamiento de datos
  - `seaborn` y `matplotlib`: Visualización

---

## Cómo Usar

1. Clona este repositorio.
   ```bash
   git clone <repository_url>
   ```

2. Instala las librerías necesarias.
   ```bash
   pip install pandas seaborn matplotlib
   ```

3. Carga el dataset (`income.csv`) en el directorio de trabajo.

4. Ejecuta el script proporcionado en un Jupyter Notebook o cualquier IDE de Python.

---

## Resultados

- Atributos como `education`, `marital-status` y `occupation` tienen una fuerte influencia en la clase de ingresos.
- Existe una correlación significativa entre `hours-per-week`, `capital-gain` y la variable objetivo (`income`).
- El preprocesamiento de datos (por ejemplo, codificación one-hot, selección de características) mejora la eficiencia en el entrenamiento del modelo.

---

## Próximos Pasos

- Implementar modelos de aprendizaje automático (por ejemplo, KNN, Regresión Logística, Random Forest) para predecir la clase de ingresos.
- Evaluar los modelos utilizando métricas como precisión, recall, y F1-score.
- Optimizar la selección de características e hiperparámetros del modelo.

---

## Estructura del Proyecto

```plaintext
adult-income-prediction/
├── data/
│   └── income.csv
├── notebooks/
│   └── EDA_and_Preprocessing.ipynb
├── scripts/
│   └── data_preprocessing.py
├── README.md
```


# Income_Prediction-Project
