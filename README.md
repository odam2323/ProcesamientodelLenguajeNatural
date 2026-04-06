# Sistema de Búsqueda y Análisis de Sentencias Jurídicas con Transformers

Este repositorio contiene la entrega final del proyecto enfocado en la creación de un algoritmo diseñado para responder preguntas jurídicas basándose en un corpus de documentos legales. 

## 🎯 Objetivo del Proyecto

El objetivo principal es desarrollar una herramienta de asistencia para abogados que necesiten encontrar fragmentos precisos y lugares puntuales dentro de textos legales para responder a preguntas específicas. Esta herramienta busca optimizar el tiempo de investigación al sugerir los documentos adecuados que se pueden citar para fundamentar una respuesta jurídica.

## 🛠️ Tecnologías y Librerías Utilizadas

El proyecto fue desarrollado en Python utilizando diversas librerías modernas de análisis de datos y procesamiento de lenguaje:
* **Procesamiento de Lenguaje Natural (NLP) y Texto:** `spacy` (utilizando el modelo en español `es_core_news_sm`), `langdetect` para detección de idioma, y `unidecode`.
* **Modelos de Lenguaje / Embeddings:** Librería `sentence-transformers` de Hugging Face para transformar los textos en representaciones vectoriales densas.
* **Machine Learning & Clustering:** `scikit-learn` para el entrenamiento del modelo de agrupamiento KMeans y el cálculo de métricas de desempeño.
* **Manejo de Datos y Visualización:** `pandas`, `numpy`, `matplotlib`, `seaborn` y la librería `datasets` para la ingesta y exploración del corpus documental.

## ⚙️ Metodología

1. **Análisis Exploratorio y Limpieza:** Se realizó un análisis descriptivo del corpus, identificando variables como la longitud de los documentos (a nivel de caracteres y palabras), el ratio de ruido y la distribución de etiquetas para evaluar un posible desbalanceo.
2. **Generación de Embeddings:** Se utilizaron modelos Transformer pre-entrenados para extraer las características semánticas de las sentencias.
3. **Agrupamiento (Clustering):** Tras vectorizar los textos, se aplicó el algoritmo de aprendizaje no supervisado KMeans (configurado con 5 clusters) para agrupar los documentos según su similitud semántica.
4. **Evaluación del Modelo:** La calidad y separación de los clusters formados se evaluó internamente utilizando el *Silhouette Score* y el índice *Davies-Bouldin*.

## 👥 Equipo de Trabajo

* **David Alejandro Agudelo Castillo**
* **Andrés Felipe Serrano Medina**
* **Ivan Yesid Sepulveda Paez**
