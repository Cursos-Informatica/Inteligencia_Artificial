## Aprendizaje Supervisado - Regresion Logistica - Clasificación

El aprendizaje supervisado consiste en encontrar una función ℎ (hipótesis) que aproxime la función real 𝑓(𝑥) a partir de un conjunto de entrenamiento con pares de entrada-salida. Esta hipótesis se elige dentro de un espacio de hipótesis 𝐻, que puede incluir funciones lineales, polinomiales, lógicas, entre otras.

<p align="center">
<img src="img/modelo.png" width="500">
</p>

La función resultante es utilizada posteriormente para predecir valores a partir de ejemplos de datos no etiquetados.

### Selección de conjunto de datos

El conjunto de datos son pares de datos etiquetados, en este caso un analista indicará en función a la experiencia el etiquetado de datos.

P.e. en el caso conjunto de datos para la detección de correos Spam, el conjunto de datos sería de la siguiente forma.

|email(x) |etiqueta(y)|
|---------|-----------|
|email1   |1          |
|email2   |0          |
|email3   |1          |
|...      |...        |

donde:
x = variables de entrada
y = variables de salida
(x,y) =  ejemplo de entrenamiento

0 : Clase Negativa (Correo legitimo)
1 : Clase Positiva (Correo Spam)



### Representacion
- Se puede basar en conocimiento previo o en un análisis exploratorio de datos (gráficos, pruebas estadísticas).
- Se pueden probar diferentes espacios y evaluar cuál se ajusta mejor.


<p align="center">
<img src="img/modelo_spam.png" width="300">
</p>



📜 Origen de la función logística
La función logística proviene del campo de la biología poblacional en el siglo XIX. Fue introducida por Pierre François Verhulst en 1838 como una forma de modelar el crecimiento de poblaciones.

🔹 Problema original
Verhulst notó que las poblaciones:

Crecen rápido al inicio (crecimiento exponencial).

Pero luego se ralentizan por recursos limitados (comida, espacio).

Finalmente, se estabilizan en un límite máximo (llamado "capacidad de carga").

Este comportamiento se modela con la ecuación logística diferencial:

$$
\frac{dP}{dt} = rP\left(1 - \frac{P}{K} \right)
$$

𝑃: población.

𝑟: tasa de crecimiento.

𝐾: capacidad máxima.

La solución de esa ecuación es la función logística:
$$
P(t) = \frac{K}{1 + Ae^{-rt}}
$$

𝑃(𝑡): población en el tiempo 𝑡.

𝐾: capacidad máxima del entorno (o población límite).

𝐴: constante relacionada con la condición inicial.

𝑟: tasa de crecimiento.

$$
e^{-rt}
$$  : decaimiento exponencial.
