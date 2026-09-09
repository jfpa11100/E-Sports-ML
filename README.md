# E-Sports Biometrics & Performance — Proyecto 1

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jfpa11100/E-Sports-ML/blob/main/notebook.ipynb)

Proyecto 1 del curso **Énfasis III: Inteligencia Artificial** — Universidad de Medellín (UdeM).
Profesor: Antonio Jesús Tamayo Herrera. Semestre 2026-1.

## Integrantes
- Mariana Pineda Isaza
- Juan Pablo Ramírez
- Juan Felipe Palacio

## Descripción

Proyecto de clasificación de Machine Learning sobre el dataset [E-Sports Biometrics & Performance](https://www.kaggle.com/datasets/sarveshchhetri/e-sports-biometrics-and-performance) (Kaggle), 250,000 registros sintéticos que simulan factores fisiológicos y ambientales de jugadores de e-sports (ritmo cardíaco, sueño, fatiga, cafeína, etc.) y su relación con el rendimiento y resultado de las partidas.

**Variable de salida:** `Match_Outcome` (Win / Loss) — problema de clasificación binaria.

El proyecto compara modelos de **Regresión Logística** y **SVM**, ambos entrenados con validación cruzada de 10 folds y distintas configuraciones de hiperparámetros (incluyendo distintos kernels para SVM), evaluados con Precision, Recall y F1.

## Estado del proyecto

- [x] Selección del dataset y descripción detallada
- [x] Análisis exploratorio de datos (EDA)
- [x] Tratamiento de valores faltantes
- [x] Preprocesamiento (encoding, escalado, split train/test)
- [x] Regresión Logística con validación cruzada (10 folds) y grid de hiperparámetros
- [x] SVM con validación cruzada (10 folds) y grid de kernels
- [ ] Comparación final de modelos y selección del mejor

### Resultados preliminares

| Modelo | F1 (CV, 10 folds) | Accuracy (test) |
|---|---|---|
| Regresión Logística | 0.415 | 0.53 |
| SVM (kernel lineal) | 0.469 | 0.52 |

Ambos modelos rinden apenas por encima del azar, consistente con el EDA: ninguna variable individual separa bien las clases Win/Loss. El análisis y la comparación final se agregarán al notebook próximamente.

## Estructura del repositorio
E-Sports-ML/
├── data/
│ └── esports_gaming_biometrics_250k.csv # Dataset principal (250k registros)
├── notebook.ipynb # Notebook principal del proyecto
└── README.md

## Cómo abrir el notebook

Haz clic en el badge "Open in Colab" arriba, o visita:
https://colab.research.google.com/github/jfpa11100/E-Sports-ML/blob/main/notebook.ipynb

## Dataset
Fuente: [Kaggle — E-Sports Biometrics & Performance](https://www.kaggle.com/datasets/sarveshchhetri/e-sports-biometrics-and-performance) (licencia CC BY-SA 4.0, datos sintéticos generados por Sarvesh Chhetri).
EOF