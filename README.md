# 🎬 Análisis de Sentimiento y NLP en Reseñas de Películas

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![NLP](https://img.shields.io/badge/NLP-spaCy%20%7C%20NLTK-green)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn%20%7C%20LightGBM-orange)
![Deep Learning](https://img.shields.io/badge/Deep%20Learning-BERT%20%7C%20PyTorch-red)

## 📌 Descripción del Proyecto
Este proyecto desarrolla un sistema de **Procesamiento de Lenguaje Natural (NLP)** diseñado para clasificar automáticamente reseñas de películas como positivas o negativas. La solución permite automatizar la moderación de contenido y el análisis de *feedback* a gran escala, asegurando alta precisión computacional.

El objetivo central del proyecto fue superar el umbral de **F1 Score de 0.85**, evaluando la relación entre la complejidad de distintos algoritmos y su costo computacional en entornos de recursos limitados.

## ⚙️ Tecnologías y Herramientas Utilizadas
* **Manipulación de Datos:** `pandas`, `numpy`
* **Procesamiento de Lenguaje Natural (NLP):** `NLTK`, `spaCy` (Lematización avanzada)
* **Modelado de Machine Learning:** `scikit-learn` (Regresión Logística, TF-IDF), `LightGBM`
* **Modelado de Deep Learning:** `PyTorch`, `transformers` (Hugging Face - Modelo BERT)

## 🧠 Enfoque y Metodología
Se implementó un desarrollo iterativo, aumentando la complejidad del procesamiento y de los algoritmos para encontrar el punto óptimo de eficiencia:

1. **Modelo Base (TF-IDF + Logistic Regression):** Preprocesamiento básico con expresiones regulares y vectorización por frecuencias.
2. **Modelo Avanzado (spaCy + TF-IDF + Logistic Regression):** Lematización profunda para normalizar el vocabulario, agrupando variaciones gramaticales y reduciendo la dimensionalidad.
3. **Ensamble de Árboles (LightGBM):** Uso de *Gradient Boosting* para capturar interacciones no lineales complejas en la matriz dispersa.
4. **Deep Learning (BERT):** Extracción de *embeddings* contextuales de 768 dimensiones para capturar el significado semántico profundo de cada oración.

## 📊 Resultados Clave
El proyecto superó el objetivo establecido con éxito, arrojando conclusiones determinantes sobre la eficiencia en Data Science:

| Modelo | Preprocesamiento | Algoritmo | F1 Score (Test) | Costo Computacional |
| :--- | :--- | :--- | :---: | :---: |
| **Modelo 1** | Limpieza Básica + TF-IDF | Regresión Logística | > 0.88 | Muy Bajo |
| **Modelo 3** | Lematización (spaCy) + TF-IDF | Regresión Logística | **Óptimo** | Bajo |
| **Modelo 4** | Lematización (spaCy) + TF-IDF | LightGBM | > 0.85 | Alto |
| **Modelo 9** | Transformadores (Hugging Face) | BERT Embeddings + LR | N/A (Muestra) | Extremo |

**Conclusión Técnica:** El Modelo 3 demostró ser la solución más pragmática. Comprobó que una excelente ingeniería de características (lematización con spaCy) combinada con un modelo lineal simple y escalable es superior a implementar redes neuronales pesadas (BERT) cuando se opera bajo restricciones de hardware (entornos sin GPU).

## 🚀 Instalación y Reproducción

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/tu-usuario/clasificacion-sentimiento-nlp.git](https://github.com/tu-usuario/clasificacion-sentimiento-nlp.git)
   cd clasificacion-sentimiento-nlp
