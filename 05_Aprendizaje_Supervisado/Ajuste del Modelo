## Ajuste del modelo


### Función de coste - Error Cuadrático Medio

Se debe minimizar una función de coste J($$\theta$$), para obtener los parámetros óptimos.

https://www.youtube.com/watch?v=lkGyu70gAzE

Para graficar la función del Error Cuadrático Medio, debemos expresar la función en base a la función hipotesis de la regresión.

Dado un conjunto de datos $$(x_{i},y_{i})$$, el modelo lineal $$h_{\theta}(x_{i})=\theta_{0}+\theta_{1}*x_{i}$$

$$
\text{ECM}(m, b) = \frac{1}{n} \sum_{i=1}^{n} \left( y_i - (mx_i + b) \right)^2
$$

Esta función es una parábola respecto a los parámetros 𝑚 y 𝑏, porque:

- El ECM es una suma de cuadrados → siempre convexa.
- Es una función cuadrática respecto a 𝑚 y 𝑏.

Visualizar la parabola del ECM

```
import numpy as np
import matplotlib.pyplot as plt

# Datos de ejemplo
x = np.array([1, 2, 3, 4])
y = np.array([2, 4, 6, 8])

# Exploramos diferentes pendientes m, con b = 0 fijo
m_values = np.linspace(0, 4, 100)
ecm_values = []

for m in m_values:
    y_pred = m * x  # b = 0
    ecm = np.mean((y - y_pred) ** 2)
    ecm_values.append(ecm)

# Graficar la parábola de ECM
plt.plot(m_values, ecm_values)
plt.title("Error cuadrático medio vs pendiente m")
plt.xlabel("Pendiente (m)")
plt.ylabel("ECM")
plt.grid(True)
plt.show()
```


### Función de Optimización - Gradiente descendente


https://www.youtube.com/watch?v=za61eVtq2MY