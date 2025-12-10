# Desarrollo, entrenamiento y optimización de dos modelos de aprendizaje profundo

Proyecto de la materia **Redes Neuronales y Sistemas Difusos**.  
El repositorio contiene dos experimentos prácticos de aprendizaje profundo:

1. **Modelo CNN aplicado a CIFAR-10**  
2. **Modelo RNN aplicado a IMDB**  

El objetivo general es **desarrollar, entrenar y optimizar** ambos modelos, comparar su desempeño y analizar sus errores.

---

## 1. Experimento CNN – Clasificación de imágenes (CIFAR-10)

- Carpeta: `cnn_cifar10/`  
- Tarea: clasificación de imágenes en 10 clases (avión, auto, pájaro, etc.).  
- Arquitecturas evaluadas:

  - **C1 – CNN baseline**  
    Arquitectura sencilla sin capas de normalización ni regularización.
  - **C2 – CNN profunda con BatchNorm y Dropout**  
    Se incrementa la profundidad y se añaden técnicas para mejorar la
    generalización.
  - **C3 – C2 + Data Augmentation**  
    Se incorpora aumento de datos (rotaciones, flips, zoom, etc.)
    para hacer el modelo más robusto.

- Resultados:
  - Curvas de **pérdida y exactitud (train/val)** para cada configuración.
  - **Matriz de confusión** y ejemplos de imágenes mal clasificadas.
  - Registro de experimentos en un archivo CSV (configuración + métricas).

---

## 2. Experimento RNN – Análisis de sentimiento (IMDB)

- Carpeta: `rnn_imdb/`  
- Tarea: clasificación de reseñas de películas como **positivas** o **negativas**.  
- Modelos recurrentes evaluados:

  - **R1 – SimpleRNN**  
    Modelo base para capturar dependencias cortas en secuencias.
  - **R2 – LSTM con Dropout**  
    Celdas LSTM para manejar dependencias de largo plazo.
  - **R3 – BiLSTM con Dropout**  
    Procesamiento bidireccional de la secuencia para aprovechar
    contexto pasado y futuro.

- Resultados:
  - Curvas de **pérdida y exactitud (train/val)**.
  - Cálculo de **accuracy** y **F1-score**.
  - Ejemplos de reseñas mal clasificadas para analizar los límites
    de cada modelo.
  - Registro de experimentos en CSV con hiperparámetros y métricas.

---

## 🛠 Instalación y ejecución

### 1️⃣ Crear entorno virtual (opcional, recomendado)

```bash
python -m venv venv
# Linux / MacOS
source venv/bin/activate
# Windows
venv\Scripts\activate
