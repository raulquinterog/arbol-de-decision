# 🌸 Análisis del Dataset Iris con LDA y Árboles de Decisión


## 📌 Descripción del Proyecto


Este proyecto analiza el famoso conjunto de datos Iris utilizando dos enfoques de clasificación:

1. Análisis Discriminante Lineal (LDA)
   
2. Árboles de Decisión
   
El objetivo es comparar ambos modelos en términos de precisión y visualización de la partición del espacio de decisión.

# 📂 Estructura del Proyecto

 📄 Iris_LDA_DecisionTree.ipynb → Notebook principal con todo el análisis.

# ⚙️ Pasos del Análisis

## 1️⃣ Carga y Preparación de Datos

Se carga el dataset Iris desde sklearn.datasets.

Se convierte en un DataFrame de Pandas.

Se divide en conjunto de entrenamiento (80%) y prueba (20%) manteniendo un balance de clases.

## 2️⃣ Regresión Logística para Selección de Variables

Se entrena un modelo de regresión logística con LogisticRegression de sklearn.

Se seleccionan las dos variables más importantes para el análisis:

Petal Length (cm)

Petal Width (cm)

## 3️⃣ Modelo de LDA y Visualización

Se entrena un modelo de Análisis Discriminante Lineal (LDA) con LinearDiscriminantAnalysis.

Se grafica la distribución de clases en función de las dos variables seleccionadas.

## 4️⃣ Modelo de Árbol de Decisión y Poda

Se entrena un Árbol de Decisión con DecisionTreeClassifier.

Se intenta podar automáticamente con ccp_alpha, pero no fue necesario.

Se realiza poda manual (max_depth=3) para evitar sobreajuste.

Se grafica la partición del espacio del árbol podado.

## 5️⃣ Evaluación de Modelos

Se comparan LDA y Árbol de Decisión con las métricas de clasificación:

* Exactitud

* Precisión

* Recall

* F1-score

Resultados:

LDA obtuvo una exactitud de 93.33%.

Árbol de Decisión podado alcanzó 96.67%, siendo el modelo con mejor rendimiento.

# 📊 Conclusiones

✅ Ambos modelos clasifican correctamente los datos de Iris.

✅ LDA es simple y efectivo cuando las clases son linealmente separables.

✅ Árbol de Decisión logra un mejor desempeño al capturar relaciones más complejas.

✅ En este caso, el Árbol de Decisión es la mejor opción con una precisión superior.
