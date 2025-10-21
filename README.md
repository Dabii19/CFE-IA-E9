# CFE-IA-E9

## Clasificación de Sentimientos con Regresión Logística

Este proyecto utiliza un conjunto de datos de textos etiquetados con emociones para entrenar un modelo capaz de predecir el sentimiento o emoción presente en nuevos textos.

## Objetivo

Entrenar un modelo de clasificación que identifique la emoción expresada en un texto (por ejemplo, alegría, tristeza, enojo, etc.) y generar un archivo de predicciones con los resultados obtenidos sobre un conjunto de prueba.

## Datos

Variables utilizadas en el modelo:

text: texto del usuario o frase a analizar.

emotion: etiqueta que representa el sentimiento asociado al texto (variable objetivo).

El conjunto de datos se dividió en un 90% para entrenamiento y un 10% para prueba, asegurando así una evaluación confiable del modelo.

## Pasos realizados

### Carga y preprocesamiento de datos

Se cargaron los archivos dataset_train.csv y dataset_test_sin_sentimento.csv.

Se verificaron valores nulos, sin encontrar datos faltantes.

Se eliminaron las filas duplicadas para evitar sesgos en el entrenamiento.

Se seleccionaron las variables text y emotion para la clasificación.

Se dividió el dataset en conjuntos de entrenamiento y prueba (90% y 10% respectivamente).

### Vectorización del texto

Se utilizó CountVectorizer para transformar los textos.

### Entrenamiento del modelo

Se empleó el modelo de Regresión Logística para la clasificación de los sentimientos.

Una vez entrenado, se evaluó su desempeño sobre el conjunto de prueba.

### Evaluación del modelo

La métrica utilizada fue la exactitud (accuracy), que mide el porcentaje de aciertos del modelo.

Se obtuvo un resultado satisfactorio, demostrando que el modelo logra clasificar correctamente la mayoría de los textos con un promedio de 50%.

## Predicciones y generación de archivo final

El modelo generó las predicciones correspondientes para cada texto.

Finalmente, se creó el archivo dataset_test_prueba.csv con las columnas:

ID: identificador del texto.

sentimiento: emoción o sentimiento predicho por el modelo.

## Resultados

El modelo de Regresión Logística alcanzó un buen nivel de exactitud general, mostrando una correcta capacidad para distinguir entre distintas emociones a partir del texto.
Si bien el enfoque es básico, los resultados demuestran la eficacia del preprocesamiento y del vectorizador de conteo para tareas de análisis de sentimientos.
