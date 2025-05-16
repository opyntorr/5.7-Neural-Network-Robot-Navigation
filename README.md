# Clasificación de Acciones del Robot SCITOS G5 con Redes Neuronales

Este proyecto implementa un modelo de red neuronal MLP (Perceptrón Multicapa) para clasificar las acciones que debe realizar un robot SCITOS G5 en función de las lecturas de sus sensores ultrasónicos.

## Archivos

- `sensor_readings_24.data`: Conjunto de datos original (24 sensores + etiqueta).
- `mlp_robot_navigation.py` o notebook `.ipynb`: Código completo para entrenamiento, evaluación y visualización.

## Descripción del Proyecto

El modelo recibe como entrada un vector de 24 lecturas ultrasónicas, y predice una de las siguientes acciones:

- `Move-Forward`
- `Sharp-Right-Turn`
- `Slight-Left-Turn`
- `Slight-Right-Turn`

Se utilizan técnicas de preprocesamiento, entrenamiento y análisis como:

- Escalado de características con `StandardScaler`
- Codificación de etiquetas con `LabelEncoder`
- División en conjunto de entrenamiento y prueba
- Entrenamiento de un MLP de 5 capas ocultas con `scikit-learn`
- Análisis de métricas como precisión, recall y F1-score
- Visualizaciones: histograma, boxplot, curva de pérdida, PCA y matriz de confusión

## Visualizaciones Generadas

- `loss_curve.png`: Curva de pérdida del MLP durante entrenamiento
- `histogramas_sensores.png`: Histogramas de los 24 sensores
- `matriz_confusion.png`: Matriz de confusión del modelo
- `pca_2d.png`: Visualización en 2D con reducción de dimensiones (PCA)
- `estructura_mlp.png`: Diagrama de la arquitectura de la red neuronal

## Requisitos

- Python 3.8+
- `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`