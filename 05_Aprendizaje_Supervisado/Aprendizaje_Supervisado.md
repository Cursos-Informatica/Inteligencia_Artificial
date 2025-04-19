## Aprendizaje Supervisado

El aprendizaje supervisado consiste en encontrar una función ℎ (hipótesis) que aproxime la función real 𝑓(𝑥) a partir de un conjunto de entrenamiento con pares de entrada-salida. Esta hipótesis se elige dentro de un espacio de hipótesis 𝐻, que puede incluir funciones lineales, polinomiales, lógicas, entre otras.

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

__Sesgo, Varianza y Sobreajuste__

- Sesgo: Restricción del espacio de hipótesis que impide capturar la complejidad real de los datos (subajuste).
- Varianza: Sensibilidad del modelo a pequeños cambios en los datos de entrenamiento (sobreajuste).
- Compensación sesgo-varianza: Modelos más simples pueden generalizar mejor, mientras que modelos muy complejos pueden ajustarse demasiado a los datos de entrenamiento y fallar en datos nuevos.

__Principio de Simplicidad y Aprendizaje Profundo__

- Navaja de Ockham: Se prefiere la hipótesis más simple que explique los datos.
- Aprendizaje profundo: Aunque las redes neuronales tienen muchos parámetros, pueden generalizar bien con suficiente datos y computación eficiente.

__Expresividad vs. Complejidad__
Modelos más expresivos pueden representar mejor los datos, pero encontrar una buena hipótesis en ellos puede ser computacionalmente difícil. Se buscan representaciones balanceadas entre expresividad y eficiencia de cómputo.


### Descargar archivos de trabajo
- Casos Practico - [Descargar](https://drive.google.com/file/d/1WQy0Ggc0EUJSDx7n6RhJz78fgjSwOZwr/view?usp=sharing)
- Datos - [Descargar](https://drive.google.com/file/d/1NhlzPS0VeVj4x1oSFYHK3t-5IArzF2Vh/view?usp=sharing)

