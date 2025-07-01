## Neurona de McCulloch y Pitts (Neurona M-P)

- Se corresponde con la primera neurona artificial de la historia. Propuesto en 1943.
- Se caracteriza porque recibe uno o más valores binarios {1,0} y retorna otro valor binario {1,0}
- Activa su salida cuando más de un número determinado de valores de entrada se encuentran activos
- Debe establecerse manualmente el número de valores de entrada que deben estar activos, a este valor se le denomina threshold

<p align="center">
<img src="img/img_01.png" width="500">
</p>

Explicacion del modelo  de McCulloch y Pitts
https://www.youtube.com/watch?v=JaLMcVO1CCE

Ejemplo simple


```
#importar libreria
import numpy as np
```

```
# implemente la función del modelo M-P sin usar funciones predefinidas de numpy

def neuronaMP(E,I,u):
    for ini in I:
        if ini == 1:
            return 0
    
    integracion = 0
    for ex in E:
        integracion = integracion + ex

    if integracion >= u:
        return 1
    else:
        return 0
```

```
# parametros
E=[1]
I=[0]
u=1

# Ejecución del modelo
print(neuronaMP(E,I,u))
```

https://www.youtube.com/watch?v=SU-44XQPh9w


## Perceptron

- Propuesto por Frank Rosenblatt en 1958
- En 1969 fue refinado y analizado en detalle por Marvin Minsky y Seymour Papert
- Mejora el planteamiento de la neurona de McCulloch y Pitts añadiendo el concepto de "peso" numérico a las entradas y planeando un mecanismo para ajustarlos
- No recibe únicamente valores de entrada binarios, permite valores de entrada reales
- Se basa en un tipo de neurona artificial conocida como Threhold Logic Unit (TLU)
- La TLU computa una suma parametrizada de las entradas

### Threshold Logic Unit - TLU

- La TLU computa una suma parametrizada de las entradas
- Después, aplica una función de activación sobre la suma calculada anteriormente

<p align="center">
<img src="img/img_02.jpeg" width="500">
</p>

- El perceptrón se corresponde con una arquitectura copuesta por una única capa de tlUs
- Permite la clasificación de instancias en diferentes clases binarias de manera simultánea

<p align="center">
<img src="img/img_03.jpeg" width="500">
</p>

### Funciones de activación

- El perceptrón permite la clasificación de instancias en clases binarias de manera simultánea
- Existen múltiples funciones de activación. Algunas de las más comunes son:


- Heaviside step function

```
        heaviside(z) = { 0 if z < 0
                         1 if z >= 0

```
- Sign function

```
                    -1 if z < 0
        sgn (z) = {  0 if z = 0
                     1 if z > 0
```


### Entrenamiento del perceptrón

1. Actualización de los pesos:

$$
w_i \leftarrow w_i + \eta \cdot (y_{\text{real}} - y_{\text{pred}}) \cdot x_i
$$

𝑤𝑖 : peso actual de la entrada 𝑖
𝜂: tasa de aprendizaje (learning rate), un valor pequeño como 0.1

𝑦 real : etiqueta verdadera (0 o 1)

𝑦 pred : salida del perceptrón (0 o 1)

𝑥𝑖 : valor de entrada correspondiente al peso 𝑤𝑖
​
 
2. Actualización del sesgo (bias):

$$
b \leftarrow b + \eta \cdot (y_{\text{real}} - y_{\text{pred}})
$$


### Componentes de una Red Neuronal Artificial

<p align="center">
<img src="img/img_05.jpeg" width="500">
</p>


### Perceptron Multicapa

- El perceptrón Multicapa o __Deep feedforward network__ es el modelo más popular dentro del Deep Learning.
- Se deonomian feedforward porque la información fluye desde las entradas hasta la salida sin conexiones de feedback
- Se caracterizan por la composición de numerosas funciones.

<p align="center">
<img src="img/img_04.jpeg" width="500">
</p>

- Que es una red neuronal

https://www.youtube.com/watch?v=jKCQsndqEGQ

- Como aprenden las redes neuronales

https://www.youtube.com/watch?v=mwHiaTrQOiI







