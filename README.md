[Acceso a archivo Jupyter.](https://github.com/mantiads/trasnformers/blob/main/1_5_fine_tunned.ipynb)

# <p align="center"> Análisis de Sentimientos en Español mediante Finetuning de Transfer Learning.</p>


El proyecto se centra en la mejora de un modelo de lenguaje pre-entrenado para realizar análisis de sentimientos en comentarios en español, utilizando el proceso de finetuning. Este enfoque aprovecha los beneficios del transfer learning, que permite transferir el conocimiento previamente adquirido por un modelo pre-entrenado a una tarea específica, y luego afinarlo con datos adicionales para mejorar su desempeño.

Inicialmente, se selecciona el modelo pre-entrenado "BSC-TeMU/roberta-base-bne", diseñado para procesamiento de lenguaje natural en español. Se prepara un conjunto de datos de comentarios de clientes de Amazon en español, donde los comentarios están etiquetados en cinco categorías de sentimientos. Sin embargo, se simplifica la tarea agrupando las categorías en dos: negativas y positivas.

Antes del finetuning, el modelo tiene un accuracy de 0.5 en el conjunto de datos de validación, lo que indica un rendimiento aleatorio o poco mejor que una predicción al azar. Luego, se procede a entrenar el modelo mediante finetuning, ajustando sus parámetros con los datos de entrenamiento y validación específicos de la tarea de clasificación de sentimientos.

Después de dos épocas de entrenamiento, el modelo finetuned logra un impresionante accuracy del 0.93 en el conjunto de datos de validación. Esta mejora significativa en el rendimiento del modelo demuestra la efectividad del finetuning para adaptar un modelo pre-entrenado a una tarea específica y mejorar su capacidad de generalización y precisión.

El motivo de elegir el accuracy como métrica de evaluación se debe a que los datos están balanceados, es decir, hay una distribución uniforme de ejemplos en las diferentes clases de sentimientos. En este contexto, el accuracy proporciona una medida sencilla y efectiva de la precisión general del modelo en la clasificación correcta de los comentarios en sentimientos negativos y positivos.

Los beneficios del transfer learning y el finetuning son evidentes en este proyecto. En primer lugar, el uso de un modelo pre-entrenado proporciona una base sólida de conocimiento lingüístico que puede ser aprovechada para una amplia gama de tareas de procesamiento de lenguaje natural en español. Este enfoque ahorra tiempo y recursos al evitar la necesidad de entrenar un modelo desde cero.

Además, el finetuning permite adaptar el modelo pre-entrenado a una tarea específica, como la clasificación de sentimientos, mediante el ajuste de sus parámetros con datos adicionales. Esto mejora la capacidad del modelo para capturar los matices y complejidades del lenguaje en la tarea específica, lo que se refleja en un mejor rendimiento en la precisión de las predicciones.

Una vez guardado el modelo, lo podemos cargar para realizar previsiones.
