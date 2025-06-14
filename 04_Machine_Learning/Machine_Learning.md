# Introducción al Aprendizaje Automático (Machine Learning)

¿Por qué queremos que una máquina aprenda? ¿Por qué no programarla directamente con la solución? Hay dos razones principales:

- Los desarrolladores no pueden anticipar todas las situaciones futuras. Por ejemplo, un robot que navega laberintos debe aprender el diseño de cada nuevo laberinto.

- A veces los desarrolladores no saben cómo programar la solución. Por ejemplo, las personas reconocen caras de familiares de manera subconsciente, pero es difícil programar esa habilidad sin usar algoritmos de aprendizaje automático.

__¿Que es el Machine Learning?__
"El apredizaje automático es un subdominio de la Inteligencia Artificial que proporciona a los sistemas la capacidad de aprender y mejorar automáticamente a partir de la experiencia __sin ser programados explícitamente.__ Se basa en la hipótesis subyacente de __crear un modelo__ y tratar de __mejorarlo ajustando más datos en el modelo__ a lo largo del tiempo"
-Arthur Samuel 

Ejemplo:
Se plantea la construcción de un filtro capaz de identificar y bloquar correos de SPAM.

Un analista deberá definirá un motor reglas para extraer los correos spam. Pero con el paso del tiempo se pueden ir desactualizando las reglas.

<p align="center">
<img src="img/spam.png" width="500">
</p>

Un analista va a componer un conjunto de datos que son SPAM y define un algoritmo de machine learning y procede a entrenarlo, es proceso se denomina definición del modelo capaz de realizar predicciones. 

<p align="center">
<img src="img/spam_01.png" width="500">
</p>


__¿Cuándo utilizar Machine Learning?__
- En soluciones que funcionan mediante la aplicación de un conjunto extenso de reglas o heurísticas
- En problemas complejos en los que un analistas no es capaz de determinar una solución a partir de la información existente
- En entornos que fluctúan o varian con frecuencia
- Apoyo de la fase de análisis en enfoques tradicionales en los que se dispone de conjuntos de datos muy grandes y dificiles de interpretar


__Aplicaciones del Aprendizaje Automático__

El aprendizaje automático es una parte esencial del desarrollo de software. Ejemplos incluyen:
- Aceleración del análisis de imágenes astronómicas en un factor de 10 millones.
- Reducción del consumo energético en centros de datos en un 40%.
- Mejora de arquitecturas de computación según Google AI.


## Tipos de los sistemas de Machine Learning

https://www.youtube.com/watch?v=oT3arRRB2Cw


__Formas de Aprendizaje__


- __Aprendizaje supervisado__: El agente aprende a partir de ejemplos etiquetados (ej. reconocer peatones en imágenes).
- __Aprendizaje no supervisado__: Encuentra patrones sin etiquetas explícitas (ej. agrupar imágenes similares).
- __Aprendizaje por refuerzo__: Aprende de recompensas y castigos (ej. mejorar su estrategia en ajedrez).

__Inducción vs. Deducción__
La inducción generaliza a partir de datos (ej. "el sol siempre ha salido, lo hará mañana"), pero no garantiza certeza, a diferencia de la deducción lógica.

 Un ejemplo de deducción es el silogismo. Por ejemplo, "Todos los hombres son mortales (premisa mayor); Sócrates es hombre (premisa menor); luego, Sócrates es mortal (conclusión)". 


__Modelos de Aprendizaje__
El aprendizaje puede manejar datos representados como vectores de atributos (factored), estructuras atómicas o modelos relacionales. Según la naturaleza de la salida, el problema puede clasificarse como:

- Clasificación: Predicción de valores discretos (ej. spam/no spam).

- Regresión: Predicción de valores numéricos (ej. temperatura del día siguiente).

Este capítulo sienta las bases para entender cómo los agentes pueden aprender y mejorar su rendimiento a partir de la experiencia.

__Tipos de Modelos__

| Categoría         | Subcategoría     | Algoritmo / Modelo                      | Año    | Creador                          | Uso                                          |
|-------------------|------------------|-----------------------------------------|--------|----------------------------------|-----------------------------------------------|
| Machine Learning  | Machine Learning | PCA                                     | 1901   | Karl Pearson                    | Reducción de dimensionalidad                 |
| Machine Learning  | Machine Learning | Regresión Lineal                        | 1805   | Adrien-Marie Legendre           | Predicción de valores continuos              |
| Machine Learning  | Machine Learning | K-Means Clustering                      | 1957   | Stuart Lloyd                    | Agrupamiento no supervisado                  |
| Machine Learning  | Machine Learning | Regresión Logística                     | 1958   | David Cox                       | Clasificación binaria                        |
| Machine Learning  | Machine Learning | k-Nearest Neighbors (k-NN)             | 1951   | Fix y Hodges                    | Clasificación basada en vecinos              |
| Machine Learning  | Machine Learning | Naive Bayes                             | 1960   | Thomas Bayes (base teórica)     | Clasificación basada en probabilidad         |
| Machine Learning  | Machine Learning | Árboles de Decisión                     | 1963   | Ross Quinlan                    | Clasificación y regresión                    |
| Machine Learning  | Machine Learning | Mean Shift Clustering                   | 1975   | Fukunaga & Hostetler            | Agrupamiento por densidad                    |
| Machine Learning  | Machine Learning | Ridge Regression                        | 1970s  | Hoerl & Kennard                 | Regresión con regularización L2              |
| Machine Learning  | Machine Learning | Lasso Regression                        | 1996   | Tibshirani                      | Regresión con regularización L1              |
| Machine Learning  | Machine Learning | AdaBoost                                | 1996   | Freund & Schapire               | Combinación de clasificadores débiles        |
| Machine Learning  | Machine Learning | DBSCAN                                  | 1996   | Ester et al.                    | Agrupamiento basado en densidad              |
| Machine Learning  | Machine Learning | Support Vector Machines (SVM)          | 1995   | Vladimir Vapnik                 | Clasificación con margen máximo              |
| Machine Learning  | Machine Learning | Gradient Boosting                       | 1999   | Friedman                        | Mejorar precisión con árboles secuenciales   |
| Machine Learning  | Machine Learning | Elastic Net                             | 2005   | Zou & Hastie                    | Regularización en modelos lineales           |
| Machine Learning  | Machine Learning | Random Forest                           | 2001   | Leo Breiman                     | Mejora predicción con múltiples árboles      |
| Machine Learning  | Machine Learning | Isolation Forest                        | 2008   | Liu et al.                      | Detección de anomalías                       |
| Machine Learning  | Machine Learning | XGBoost                                 | 2014   | Tianqi Chen                     | Boosting eficiente para grandes datasets     |
| Machine Learning  | Machine Learning | LightGBM                                | 2016   | Microsoft                       | Gradient boosting rápido y eficiente         |
| Machine Learning  | Machine Learning | CatBoost                                | 2017   | Yandex                          | Boosting con variables categóricas           |




## Laboratorio 02:

Revisar el ejercicio que se encuentra en el siguiente [enlace](/00_Laboratorio/Laboratorio02.md)







