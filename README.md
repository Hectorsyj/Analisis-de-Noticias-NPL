# Análisis de Noticias

## Entrega Final
*Actividad Evaluativa: Clasificación de Noticias Usando RNNs y LSTMs*

## Integrantes Grupo 14
* *Hector Bello Santamaria*
* *Adriana Maldonado*
* *Johanna Ramirez Londoño*
* *Leidys Valencia Bello*

---

## Descripción del Proyecto

Este proyecto tiene como objetivo principal clasificar noticias en categorías especializadas utilizando modelos de redes neuronales recurrentes (RNN) y Long Short-Term Memory (LSTM). Los modelos fueron entrenados y evaluados en un conjunto de datos preprocesado que contiene textos largos, con el fin de analizar la efectividad de estas arquitecturas en tareas de clasificación de texto.

---

## Ejercicios Realizados

### Ejercicio 1: Exploración de Datos
Se exploró la distribución de las categorías en el conjunto de datos para entender la representatividad de cada clase y garantizar que los modelos fueran entrenados en datos balanceados. Esto incluyó visualizaciones de frecuencias y cálculos descriptivos para identificar posibles sesgos en los datos originales.

---

### Ejercicio 2: Filtrado de Datos
Se seleccionaron categorías relevantes (*deportes, **economía, **cultura, **justicia*) y se aplicó sobremuestreo para balancear las clases, mejorando la representatividad de las categorías menos frecuentes.

---

### Ejercicio 3: Preprocesamiento de Texto
El texto fue preprocesado siguiendo estas acciones:
- Conversiones a minúsculas.
- Eliminación de puntuación, números y espacios en blanco adicionales.
- Tokenización y padding para uniformizar las entradas a los modelos. 

Estas técnicas garantizaron datos limpios y listos para el entrenamiento de modelos de aprendizaje profundo.

---

### Ejercicio 4: División del Conjunto de Datos
El conjunto de datos preprocesado fue dividido en dos subconjuntos:
- *Entrenamiento* (80%)
- *Validación* (20%)

La división fue estratificada para mantener una proporción constante de las categorías en ambos subconjuntos. Se utilizó sobremuestreo para balancear las clases en el conjunto de entrenamiento.

---

### Ejercicio 5: Implementación de un Modelo RNN
Se implementó una red neuronal recurrente (RNN) con las siguientes características:
- Capas de embedding y capas recurrentes.
- Hiperparámetros ajustados para el problema específico.

*Conclusiones:*
- El modelo presentó buena capacidad para clasificar textos largos pero mostró inestabilidad debido a la sensibilidad a los hiperparámetros.
- Las curvas de aprendizaje evidenciaron problemas de overfitting, incluso tras aplicar estrategias como Dropout.

---

### Ejercicio 6: Construcción y Entrenamiento de Modelos LSTM
Se implementó un modelo LSTM con las siguientes características:
- Incorporación de capas bidimensionales para analizar el contexto de las palabras.
- Uso de hiperparámetros consistentes con los utilizados en el modelo RNN.

*Conclusiones:*
- El modelo LSTM permitió un aprendizaje más estable y efectivo.
- Se alcanzaron altos valores de *accuracy* tanto en el conjunto de entrenamiento como en el de validación, demostrando una mejora sustancial respecto al modelo RNN.

---

### Ejercicio 7: Comparación de Resultados
Se compararon los modelos RNN y LSTM utilizando métricas como *precisión, **recall* y *F1-score*. También se analizaron las curvas de aprendizaje de ambos modelos:
- *RNN:* Indicó problemas de generalización y susceptibilidad al overfitting.
- *LSTM:* Mostró un aprendizaje más robusto, con resultados consistentes en entrenamiento y validación.

*Conclusión General:* El modelo LSTM es más adecuado para tareas de clasificación de texto en este contexto, gracias a su capacidad de manejar relaciones a largo plazo entre palabras.

---

## Estructura del Proyecto

### Archivos y Carpetas

* *Datos/*: Conjunto de datos original utilizado para el análisis.
* *Código/*: Contiene los notebooks para preprocesamiento, entrenamiento y evaluación de los modelos.
* *Informe/*: Documentación de los resultados finales y comparación de modelos.

---

## Dependencias

Para ejecutar este proyecto, asegúrate de tener instalado lo siguiente:
- *Python 3.8 o superior*
- *TensorFlow 2.x*
- Bibliotecas adicionales:
  - numpy
  - pandas
  - scikit-learn
  - matplotlib
  - seaborn
  - imbalanced-learn
