## Aprendizaje Supervisado

El aprendizaje supervisado consiste en encontrar una función ℎ (hipótesis) que aproxime la función real 𝑓(𝑥) a partir de un conjunto de entrenamiento con pares de entrada-salida. Esta hipótesis se elige dentro de un espacio de hipótesis 𝐻, que puede incluir funciones lineales, polinomiales, lógicas, entre otras.

La función resultante es utilizada posteriormente para predecir valores a partir de ejemplos de datos no etiquetados.

<p align="center">
<img src="img/modelo.png" width="500">
</p>

El conjunto de datos son pares de datos etiquetados, en este caso un analista indicará en función a la experiencia el etiquetado de datos.

P.e. en el caso conjunto de datos para la detección de correos Spam, el conjunto de datos sería de la siguiente forma.

|email  |etiqueta|
|-------|--------|
|email1 |Spam    |
|email2 |No Spam |
|email3 |Spam    |
|...    |...     |


__Selección del Espacio de Hipótesis__

- Se puede basar en conocimiento previo o en un análisis exploratorio de datos (gráficos, pruebas estadísticas).
- Se pueden probar diferentes espacios y evaluar cuál se ajusta mejor.

__Evaluación del Modelo__

- Consistencia: Idealmente, ℎ(𝑥) debe coincidir con 𝑦 para todos los datos de entrenamiento, pero en la práctica se busca la mejor aproximación.

- Generalización: El modelo debe predecir correctamente datos nuevos, lo que se evalúa con un conjunto de prueba.

__Ejemplos de Modelos__
Distintas elecciones de 𝐻 generan diferentes ajustes a los datos:

1. Funciones lineales: Simples, pero pueden no representar bien los datos.

2. Funciones sinusoidales: Se ajustan mejor si los datos tienen periodicidad.

3. Funciones por segmentos lineales: Siguen exactamente los datos, pero pueden sobreajustar.

4. Polinomios de grado alto: Pueden ajustarse perfectamente a los datos de entrenamiento, pero tienen alto riesgo de sobreajuste.


## Laboratorio 03:

Revisar el ejercicio que se encuentra en el siguiente [enlace](/00_Laboratorio/Laboratorio03.md)



