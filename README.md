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

El proyecto compara dos modelos, ambos entrenados con validación cruzada de 10 folds y una malla de hiperparámetros, evaluados con Precision, Recall y F1:
- **Regresión Logística**, con `class_weight="balanced"`.
- **SVM (soft-margin primal, lineal)** — `LinearSVC(dual=False)`, sin kernel trick.

## Estado del proyecto

- [x] Selección del dataset y descripción detallada
- [x] Análisis exploratorio de datos (EDA)
- [x] Tratamiento de valores faltantes
- [x] Preprocesamiento (encoding, escalado, split train/test 70/30)
- [x] Regresión Logística con validación cruzada (10 folds) y grid de hiperparámetros
- [x] SVM (soft-margin primal) con validación cruzada (10 folds) y grid de hiperparámetros
- [x] Comparación final de modelos y conclusiones

### Resultados finales

| Modelo | F1 (CV, 10 folds) | Accuracy (test) |
|---|---|---|
| Regresión Logística | 0.518 | 0.53 |
| SVM (lineal, primal) | 0.518 | 0.53 |

Ambos modelos obtienen resultados prácticamente idénticos — coherente con que, sin kernel trick, SVM primal y Regresión Logística son ambos clasificadores lineales con regularización L2 fuerte (`C=0.001` ganó en los dos). El desempeño ronda apenas por encima de una predicción trivial, consistente con el EDA: solo `APM` y `Reaction_Time_ms` muestran señal predictiva real; el resto de variables biométricas aporta poco de forma individual. Ver el notebook para el análisis completo de coeficientes, matrices de confusión y conclusiones.

## Estructura del repositorio
```
E-Sports-ML/
├── data/
│ └── esports_gaming_biometrics_250k.csv # Dataset principal (250k registros)
├── notebook.ipynb # Notebook principal del proyecto
└── README.md
```

## Cómo abrir el notebook

Haz clic en el badge "Open in Colab" arriba, o visita:
https://colab.research.google.com/github/jfpa11100/E-Sports-ML/blob/main/notebook.ipynb

## Dataset
Fuente: [Kaggle — E-Sports Biometrics & Performance](https://www.kaggle.com/datasets/sarveshchhetri/e-sports-biometrics-and-performance) (licencia CC BY-SA 4.0, datos sintéticos generados por Sarvesh Chhetri).
EOF
