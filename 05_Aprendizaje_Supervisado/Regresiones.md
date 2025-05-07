## Aprendizaje Supervisado - Regresion Lineal

<p align="center">
<img src="img/modelo.png" width="500">
</p>

### Conjunto de datos de entrenamiento

|Número sistema afectado (x)  | Coste en euros (y) |
|-----------------------------|--------------------|
|1000                         | 10,000             |
|1500                         | 20,000             |
|500                          | 5,500              |
|...                          |...                 |

donde:
-  x = variables de entrada
-  y = variables de salida
-  (x,y) = ejemplo de entrenamiento

### Función de hipótesis

$$h_{\theta}(x)=\theta_{0}+\theta_{1}x$$


<p align="center">
<img src="img/reg_lineal_incidente.png" width="500">
</p>

La función hipotesis de la regresión lineal, está representada por una función generica que podria ser una linea recta en el caso de que solo se considere una caracteristica en el modelo.

Si en el conjunto de datos se considerar varias caracteristicas para la evaluación del modelo, función hipotesis sería una regresión lineal multivariable la cual se representa de la siguiente manera:

$$h_{\theta}(x)=\theta_{0}+\theta_{1}x_{1}+\theta_{2}x_{2}+...+\theta_{n}x_{n}$$

### Construcción del modelo

Para obtener la función en un regresion lineal utilizamos los siguientes comandos:

from sklearn.linear_model import LinearRegression

__Construcción del modelo y ajuste de la función hipótesis__
```
lin_reg = LinearRegression()
lin_reg.fit(df['n_equipos_afectados'].values.reshape(-1, 1), df['coste'].values)
```
donde fit entrena al modelo:
🔹 df['n_equipos_afectados']: es la variable independiente (feature)
🔹 df['coste']: es la variable dependiente (target) que se quiere predecir
🔹 .values.reshape(-1, 1): transforma la columna en un array de 2D, requerido por scikit-learn (ya que espera una matriz de entrada, no un vector unidimensional) 

__Parámetros de la función__

Los parámetros de la función $$\theta_{0}$$ y $$\theta_{1}$$ , determinan la función matematica. El objetivo es encontrar el valor optimo de esos parámetros que ajusten mejor a la tendencia de nuestros conjuntos de datos.

Para obtener estos datos se utilizan los siguientes comandos:

__Parámetro theta 0__
```
lin_reg.intercept_
```
__Parámetro theta 1__
```
lin_reg.coef_
```

### Función de coste

Se debe minimizar una función de coste J($$\theta$$), para obtener los parámetros óptimos.

https://www.youtube.com/watch?v=lkGyu70gAzE