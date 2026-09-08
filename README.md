# E-Sports Biometrics & Performance — Proyecto 1

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/JuanPa28/esports-biometrics-ml/blob/main/notebooks/proyecto1_esports_biometrics.ipynb)

Proyecto 1 del curso **Énfasis III: Inteligencia Artificial** — Universidad de Medellín (UdeM).
Profesor: Antonio Jesús Tamayo Herrera. Semestre 2026-1.

## Integrantes
- Mariana Pineda Isaza
- Juan Pablo Ramírez
- Juan Felipe Palacio

## Descripción

Proyecto de clasificación de Machine Learning sobre el dataset [E-Sports Biometrics & Performance](https://www.kaggle.com/datasets/sarveshchhetri/e-sports-biometrics-and-performance) (Kaggle), 250,000 registros sintéticos que simulan factores fisiológicos y ambientales de jugadores de e-sports (ritmo cardíaco, sueño, fatiga, cafeína, etc.) y su relación con el rendimiento y resultado de las partidas.

**Variable de salida:** `Match_Outcome` (Win / Loss) — problema de clasificación binaria.

El proyecto compara modelos de **Regresión Logística** y **SVM** entrenados con validación cruzada de 10 folds y distintas configuraciones de hiperparámetros, evaluados con Precision, Recall y F1.

> Este README y el notebook se encuentran actualmente en fase de esqueleto inicial. El desarrollo completo (EDA, modelos, comparación de resultados) se realizará en sesiones posteriores.

## Estructura del repositorio

```
esports-biometrics-ml/
├── data/
│   ├── esports_gaming_biometrics_250k.csv   # Dataset principal (250k registros)
│   └── data_dictionary.csv                  # Diccionario de variables del dataset
├── notebooks/
│   └── proyecto1_esports_biometrics.ipynb   # Notebook principal del proyecto
└── README.md
```

## Cómo abrir el notebook

Haz clic en el badge "Open in Colab" arriba, o visita:

```
https://colab.research.google.com/github/JuanPa28/esports-biometrics-ml/blob/main/notebooks/proyecto1_esports_biometrics.ipynb
```

Para guardar tus cambios de vuelta al repositorio desde Colab: **Archivo → Guardar una copia en GitHub**.

## Dataset

Fuente: [Kaggle — E-Sports Biometrics & Performance](https://www.kaggle.com/datasets/sarveshchhetri/e-sports-biometrics-and-performance) (licencia CC BY-SA 4.0, datos sintéticos generados por Sarvesh Chhetri).
