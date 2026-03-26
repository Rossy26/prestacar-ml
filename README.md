# Prestacar ML - Análisis de Riesgo Crediticio

## Descripción del Proyecto

Este proyecto consiste en la construcción de un modelo de **Machine Learning** para evaluar el riesgo crediticio de los clientes de una entidad financiera. El objetivo principal es predecir la probabilidad de que un cliente caiga en mora con su préstamo automotriz ("Prestacar"). 

Uno de los principales retos abordados en este proyecto es el manejo de **clases desbalanceadas**, dado que la gran mayoría de los clientes cumplen con sus pagos, mientras que una pequeña fracción representa a los clientes morosos.

## Datos y Características

El modelo se entrena utilizando el conjunto de datos `prestacar.csv`, el cual incluye información financiera y demográfica de los clientes, tales como:
- Ingresos del cliente.
- Anualidad del préstamo.
- Años con casa propia.
- Evaluaciones crediticias (Scores).
- Variable objetivo: `moroso` (0 = Cumplido, 1 = Moroso).

## Tecnologías Utilizadas

Las herramientas y librerías clave utilizadas para el desarrollo de este proyecto son:
- **Python**: Lenguaje de programación principal.
- **Pandas**: Para la manipulación y análisis de datos.
- **Scikit-Learn**: Para la creación, entrenamiento y evaluación de modelos de Machine Learning (ej. `DecisionTreeClassifier`).
- **Matplotlib / Seaborn**: Para la visualización de datos y resultados de las distintas métricas de evaluación.
- **Jupyter Notebook**: Como entorno de desarrollo interactivo.

## Estructura del Repositorio

```text
📦 prestacar-ml
 ┣ 📜 notebook.ipynb     # Cuaderno principal con el análisis exploratorio y entrenamiento de los modelos
 ┣ 📜 prestacar.csv      # Dataset utilizado para el entrenamiento (datos locales)
 ┣ 📜 requirements.txt   # Dependencias necesarias para ejecutar el proyecto
 ┗ 📜 README.md          # Documentación del proyecto (este archivo)
```

## Instalación y Uso

Sigue estos pasos para ejecutar el proyecto en tu entorno local:

1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/Rossy26/prestacar-ml.git
   cd prestacar-ml
   ```

2. **Crea un entorno virtual (Opcional pero recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

3. **Instala las dependencias necesarias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Ejecuta el entorno interactivo:**
   Abre el archivo `notebook.ipynb` usando Jupyter Notebook o Jupyter Lab para ver el análisis completo y ejecutar las celdas de código.
   ```bash
   jupyter notebook notebook.ipynb
   ```

## Modelado y Evaluación

El proyecto comienza estableciendo un **baseline** utilizando un `DecisionTreeClassifier`. Parte fundamental del proceso implica:
1. **División de los datos**: Separación en conjuntos de entrenamiento (`train`), validación (`val`) y prueba (`test`) para evitar el sobreajuste.
2. **Entrenamiento**: Ajuste de los modelos con los datos de entrenamiento.
3. **Métricas de Evaluación**: Análisis del rendimiento de los modelos prestándole especial atención a métricas útiles para un caso de uso con clases desbalanceadas (como precisión, recall, f1-score y la matriz de confusión), entendiendo las limitaciones de usar únicamente la exactitud (accuracy).

