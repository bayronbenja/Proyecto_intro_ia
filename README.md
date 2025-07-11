# Proyecto final introducción a la inteligencia artifical

## Descripcion del problema

Cada estudiante tiene distintos hábitos de vidas diarias como hacer ejercicios, practicar deportes o cocinar entre otros.Sin embargo estos hábitos de salud influyen en los rendimientos acádemicos sobre todo las horas de estudios y de sueño.Se incluye tambien la calificacion final del examen que determina el desempeño académico de cada estudiante.

El objetivo de este problema es como los hábitos de salud de cada estudiante afectan a su rendimiento académico considerando las calificaciones de los exámenes finales y cuales impactos se podrian generar en base a los hábitos.

## Breve descripcion del dataset y fuente

El dataset seleccionado es [https://www.kaggle.com/datasets/jayaantanaath/student-habits-vs-academic-performance], este conjunto de datos explora la relación entre los hábitos de vida (horas de sueño,horas de estudios,horas de redes sociales) y el rendimiento académico de los estudiantes y simula los hábitos diarios de 1000 estudiantes, desde el tiempo de estudio hasta la salud mental, y los compara con las calificaciones de los exámenes finales. Es como espiar tu promedio a través de la lente del estilo de vida.
Es ideal para proyectos de aprendizaje autómatico, análisis de regresión, creacion de patrones para la clasificación
Este dataset muestra 1000 observaciones (estudiantes) y 16 columnas(habitos de vida de estudiante y la calificación final de un exámen de los estudiantes)

El dataset esta tiene 9 variables numericas(edad,horas de estudios, horas de redes sociales, horas de netflix,horas de sueño, numero de asistencia a clases.) y 7 variables categoricas(genero,id estudiante,calidad de internet,educacion de los padres,participacion extracurricular).

Para el analisis exploratorio de datos, vamos a considerar dos columnas categoricas que son "genred" y
"internet_quality" y transformar a númericas ya que esto factores tambien podirian influir en el rendimiento academico de cada estudiante para la correcta prediccion del modelo.En el codigo se explicita como hacer la transformacion.También eliminaremos los valores nulos presentes en el dataset, se gráficara un histograma para todas las variables númericas y una matriz de correlación para saber como estan correlación cada variable.

Finalmente no vamos a utilizar el PCA para las feactures ya que al usar Ridge y Lasso que son los componentes del modelo de regersion lineal, se ajusta bien a los problemas

## Justificación del modelo

(Regresion Lineal)

Para este conjunto de datos, utilizaremos el método de Regresion lineal para predecir las califiaciones de los exámenes finales de cada estudiante en funcion a multiples variables independientes.Este dataset cuenta con 16 características,como la regresion lineal es un aprendizaje supervisado se puede ajustar el modelo mostrando las etiquetas para predecir los resultados finales de las califiaciones de los estudiantes.

El modelo de la regresión lineal es facil de entender y los resultados de la regresión son faciles de interpretar comprendiendo la correlación entre variables y ádemas maneja una alta cantidad de datos permitiendo tener una buena escalabilidad y visualización de los datos.

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

## Conclusiones
