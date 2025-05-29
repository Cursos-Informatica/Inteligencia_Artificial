
### 1. Ecuación diferencial logística

La forma de la ecuación es:

$$
\frac{dP}{dt}=rP(1−\frac{P}{K})
$$

Donde:

    P(t): población en el tiempo t

    r: tasa de crecimiento

    K: capacidad máxima o capacidad de carga

- Esta es una ecuación diferencial separable, así que vamos a separarla y resolverla.

### 2. Separar variables

$$
\frac{dP}{P(1−\frac{P}{K})}=r dt
$$

- Multiplicamos numerador y denominador por K para simplificar:

$$
\frac{K dP}{P(K−P)}=r dt
$$

- Ahora resolvemos la integral del lado izquierdo usando fracciones parciales.

### 3. Fracciones parciales

- Queremos escribir:

$$
\frac{K}{P(K−P)}=\frac{A}{P}+\frac{B}{K−P}
$$

- Multiplicamos ambos lados por P(K−P):

$$K=A(K−P)+BP$$

- Para encontrar A y B, igualamos coeficientes:

    Si P=0: K = A(K−0) ⇒ A = K/K ​= 1

    Si P=K: K = BK ⇒ B = K/K = 1

- Entonces:

$$
\frac{K}{P(K−P)}=\frac{1}{P}+\frac{1}{K−P}
$$


### 4. Integrar ambos lados

$$
∫\left(\frac{1}{P}+\frac{1}{K−P}\right) dP=∫r dt
$$

- El lado izquierdo:

$$
∫\frac{1}{P} dP+∫\frac{1}{K−P} dP=ln⁡∣P∣−ln⁡∣K−P∣
$$

(Nota: en la segunda integral usamos el cambio de variable u=K−P)

- Resultado de ambos lados:

$$
ln\left(\frac{P}{K−P}\right)=rt+C
$$

### 5. Despejar P(t)

- Elevamos ambos lados como potencias de ee:

$$
\frac{P}{K−P}=e^{rt+C}=Ae^{rt} (donde A=eC)
$$

- Multiplicamos ambos lados por K−P:

$$
P=Ae^{rt}(K−P)
$$

- Distribuir el lado derecho:

$$
P=AKe^{rt}−APe^{rt}
$$

- Agrupar términos con P:

$$
P+APe^{rt}=AKe^{rt}⇒P(1+Ae^{rt})=AKe^{rt}
$$

- Finalmente, despejamos P(t):

$$
P(t)=\frac{AKe^{rt}}{1+Ae^{rt}}=\frac{K}{1+\frac{1}{A}e^{−rt}}=\frac{K}{1+Be^{−rt}}
$$

donde B=1/A​ → se puede determinar con condiciones iniciales.

### 6. Ejemplo numérico

Supón:

- Capacidad de carga: K=1000K=1000
- Tasa de crecimiento: r=0.2r=0.2
- Población inicial: P(0)=100P(0)=100

Primero, calculemos B:

$$
P(0)=\frac{K}{1+B}
$$
$$
⇒100=\frac{1000}{1+B}
$$
$$
⇒1+B=\frac{1000}{100}=10
$$
$$
⇒B=9
$$

Entonces la solución es:

$$
P(t)=\frac{1000}{1+9e^{−0.2t}}
$$

Ahora evaluamos algunos valores:

|t	|P(t)    |
|---|--------|
|0	|100     |
|5	|≈ 259.2 |
|10	|≈ 500   |
|15	|≈ 740.7 |
|20	|≈ 899.7 |
|30	|≈ 980.2 |

La población crece rápidamente al principio y luego se estabiliza cerca de 1000.


Quieres graficarlo?

Aquí tienes un código en Python (Jupyter compatible):

```
import numpy as np
import matplotlib.pyplot as plt
```
```
# Parámetros
K = 1000
r = 0.2
B = 9  # calculado desde P(0) = 100
```
```
# Función P(t)
def logistic(t):
    return K / (1 + B * np.exp(-r * t))
```
```
# Tiempo
t = np.linspace(0, 30, 200)
P = logistic(t)
```
```
# Graficar
plt.plot(t, P, label='P(t)', color='blue')
plt.title('Modelo logístico de Verhulst')
plt.xlabel('Tiempo (t)')
plt.ylabel('Población P(t)')
plt.grid(True)
plt.axhline(K, linestyle='--', color='gray', label='Capacidad de carga K')
plt.legend()
plt.show()
```
__Video__

https://www.youtube.com/watch?v=G-zYV9VS1rQ

https://www.youtube.com/watch?v=gjB5bY6yikU



## Ejemplos

Ejemplo 1: Adopción de una nueva tecnología

📘 Contexto:

Cuando una nueva tecnología aparece (como un celular, IA, o una red social), la adopción sigue un patrón sigmoide: pocos al principio, luego se populariza rápido, y finalmente se estabiliza.

🔢 Fórmula logística:

$$
A(t)=\frac{K}{1+Be^{−rt}}
$$

🧪 Supuestos:

- Capacidad máxima de adopción: 100 millones de personas
- Adopción inicial: 5 millones
- Crecimiento rápido: r=0.5

📄 Código:

```
import numpy as np
import matplotlib.pyplot as plt
```
```
# Parámetros
K = 100  # millones
P0 = 5   # millones
r = 0.5
B = (K - P0) / P0
```
```
# Función de adopción
def adopcion(t):
    return K / (1 + B * np.exp(-r * t))
```
```
# Tiempo
t = np.linspace(0, 15, 200)
A = adopcion(t)
```
```
# Gráfico
plt.plot(t, A, label="Adopción (millones)", color='green')
plt.title('Adopción de tecnología con modelo logístico')
plt.xlabel('Años')
plt.ylabel('Usuarios (millones)')
plt.grid(True)
plt.axhline(K, linestyle='--', color='gray', label='Capacidad máxima')
plt.legend()
plt.show()
```

✅ Ejemplo 2: Efectividad de una medicina según la dosis

📘 Contexto:

La eficacia de un medicamento frente a una enfermedad muchas veces no crece linealmente con la dosis. En cambio, sigue una curva sigmoide: al inicio poco efecto, luego aumenta rápido, y finalmente se satura.

🧪 Supuestos:

- Dosis entre 0 y 100 mg
- Eficacia máxima: 100%
- Punto de inflexión: 50 mg
- r=0.2

📄 Código:

```
# Parámetros
K = 100  # % de eficacia
B = 1    # control de posición
r = 0.2
```

```
# Dosis
dosis = np.linspace(0, 100, 200)
```
```
# Función logística
eficacia = K / (1 + B * np.exp(-r * (dosis - 50)))
```
```
# Gráfico
plt.plot(dosis, eficacia, label="Eficacia (%)", color='blue')
plt.title('Eficacia de un fármaco según la dosis')
plt.xlabel('Dosis (mg)')
plt.ylabel('Eficacia (%)')
plt.grid(True)
plt.axhline(100, linestyle='--', color='gray', label='Máxima eficacia')
plt.legend()
plt.show()
```


✅ Ejemplo 3: Calificación de satisfacción de clientes vs. tiempo de espera

📘 Contexto:

Cuanto más esperan los clientes, menor es su satisfacción. Pero no es una línea recta: al principio no importa tanto, pero luego la molestia aumenta rápidamente.

🧪 Supuestos:

- Satisfacción de 100% si no hay espera
- Baja rápido a partir de 5 minutos
- r=−1 (negativo porque satisfacción baja)

📄 Código:

```
# Parámetros
K = 100  # satisfacción %
r = -1
B = 1
```
```
# Tiempo de espera en minutos
t = np.linspace(0, 10, 200)
```
```
# Satisfacción decrece sigmoidalmente
satisfaccion = K / (1 + B * np.exp(-r * (t - 5)))
```
```
# Gráfico
plt.plot(t, satisfaccion, label="Satisfacción (%)", color='red')
plt.title('Satisfacción de cliente vs. tiempo de espera')
plt.xlabel('Tiempo de espera (minutos)')
plt.ylabel('Satisfacción (%)')
plt.grid(True)
plt.axhline(100, linestyle='--', color='gray', label='Satisfacción inicial')
plt.legend()
plt.show()
```
