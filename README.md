# Proyecto final introducción a la inteligencia artifical

## Descripcion del problema

Cada estudiante tiene distintos hábitos de vidas diarias, como hacer ejercicios, practicar deportes o cocinar, entre otros. Sin embargo, estos hábitos de salud influyen en los rendimientos académicos, sobre todo las horas de estudio y de sueño. Se incluye también la calificación final del examen que determina el desempeño académico de cada estudiante.

El objetivo de este problema es cómo los hábitos de salud de cada estudiante afectan a su rendimiento académico, considerando las calificaciones de los exámenes finales y cuáles impactos se podrían generar con base en los hábitos.

## Breve descripcion del dataset y fuente

El dataset seleccionado es [https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance], este conjunto de datos explora la relación entre los hábitos de vida (horas de sueño, horas de estudios, horas de redes sociales) y el rendimiento académico de los estudiantes y simula los hábitos diarios de 1000 estudiantes, desde el tiempo de estudio hasta la salud mental, y los compara con las calificaciones de los exámenes finales. Es como espiar tu promedio a través de la lente del estilo de vida. Es ideal para proyectos de aprendizaje automático, análisis de regresión, creación de patrones para la clasificación.
Este dataset muestra 1000 observaciones (estudiantes) y 16 columnas (hábitos de vida de estudiante y la calificación final de un examen de los estudiantes).

El dataset cuenta con 9 variables numéricas (edad, horas de estudios, horas de redes sociales, horas de Netflix, horas de sueño, número de asistencia a clases) y 7 variables categóricas (género, ID estudiante, calidad de internet, educación de los padres, participación extracurricular).

Para el análisis exploratorio de datos, vamos a considerar dos columnas categóricas que son "genred" y "internet_quality" y transformar a numéricas, ya que estos factores también podrían influir en el rendimiento académico de cada estudiante para la correcta predicción del modelo. En el código se explicita cómo hacer la transformación. También eliminaremos los valores nulos presentes en el dataset, se graficará un histograma para todas las variables numéricas y una matriz de correlación para saber cómo están correlacionadas cada variable.

Finalmente, no vamos a utilizar el PCA para las feactures ya que al usar Ridge y Lasso que son los componentes del modelo de regresión lineal, se ajusta bien a los problemas.

## Justificación del modelo

(Regresion Lineal)

Para este conjunto de datos, utilizaremos el método de Regresion lineal para predecir las calificaciones de los exámenes finales de cada estudiante en función de múltiples variables independientes. Este dataset cuenta con 16 características. Como la regresión lineal es un aprendizaje supervisado, se puede ajustar bien el modelo buscando la línea recta que mejor ajuste a los datos para predecir los resultados finales de las calificaciones de los estudiantes.

El modelo de la regresión lineal es fácil de entender y los resultados de la regresión son fáciles de interpretar, comprendiendo la correlación entre variables y además maneja una alta cantidad de datos, permitiendo tener una buena escalabilidad y visualización de los datos.

## Metodología aplicada

- Importación de los datos
- EDA(analisis exploratorio de los datos)
- Selección de Feature
- División de los datos
- Entrenamiento de los datos
- Testeo de los datos
- Validación Cruzada
- Métricas
- Visualización de los gráficos
- Resultados obtenidos

## Resultados obtenidos

EDA: Existe una correlación de las variables puntaje examen y horas de estudio diario de forma significativa.

Para la evaluación del modelo se utilizó Cross Validation para medir el rendimiento del modelo predictivo; los resultados fueron los siguientes:

mean(promedio) cross validation: 0.896

std(desviacion estandar) cross validation: 0.026

También se utilizó cross validation usando el término polinómico de grado 2 obteniendo lo siguiente:

mean(promedio) cross validation: 0.893

std(desviación estandar) cross validation: 0.024

Se concluye que el modelo presenta un mayor desempeño predictivo sin usar el término polinomial.

Calculamos la varianza explicada o R^2 para la variabilidad de datos, utilizando los datos de entrenamiento y testeo por separado. Los resultados fueron los siguientes: r2 score(datos de entrenamiento) : 0.918, r2 score(datos de prueba): 0.886

Se deduce que el r2 de los datos de entrenamiento presenta un mayor desempeño que los datos de prueba, sin embargo, no es tan significativo dado que ambos valores de r2 son muy altos, por lo que los datos estarían sobreajustados al modelo y podría provocar resultados predichos irrelevantes al modelo y no generalizaría datos nuevos.

Finalmente se graficó el resultado de la regresión, indicando que el modelo no se ajusta muy bien a los datos, ya que tanto los valores reales(y test) y los valores predichos(y pred) se concentran en un rango específico.

## Conclusiones

Podemos concluir que estudiar más horas por día y cuidar la rutina de salud mental mejorará significativamente el rendimiento académico de los estudiantes, aunque no siempre será efectivo dado que no se constituye bien el modelo a la base de datos; por lo tanto, el resultado de las calificaciones de los estudiantes dependerá de la dificultad del examen y el tiempo planificado de los estudiantes para estudiar para el día del examen.
