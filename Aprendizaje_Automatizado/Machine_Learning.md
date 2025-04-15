# Introducción al Aprendizaje Automatizado

¿Por qué queremos que una máquina aprenda? ¿Por qué no programarla directamente con la solución? Hay dos razones principales:

Los desarrolladores no pueden anticipar todas las situaciones futuras. Por ejemplo, un robot que navega laberintos debe aprender el diseño de cada nuevo laberinto, y un programa que predice el mercado bursátil debe adaptarse a cambios económicos.

A veces los desarrolladores no saben cómo programar la solución. Por ejemplo, las personas reconocen caras de familiares de manera subconsciente, pero es difícil programar esa habilidad sin usar algoritmos de aprendizaje automático.

## Formas de Aprendizaje

Cualquier componente de un agente inteligente puede mejorarse mediante aprendizaje automático. La mejora depende de qué componente se optimiza, qué conocimiento previo posee el agente y qué datos y retroalimentación tiene disponibles.

Componentes que pueden aprenderse:

1. Reglas de acción basadas en condiciones.
2. Reconocimiento de patrones a partir de percepciones.
3. Comprensión de la evolución del mundo y efectos de las acciones.
4. Información sobre la utilidad de distintos estados.
5. Valoración de la conveniencia de diferentes acciones.
6. Definición de objetivos.
7. Sistemas de mejora como generadores de problemas y críticos.

Por ejemplo, un automóvil autónomo puede aprender cuándo frenar observando a un conductor humano o identificando autobuses en imágenes (clasificación). También puede aprender los efectos de frenar en diferentes condiciones y ajustar su conducción para mayor confort del pasajero.

__Aplicaciones del Aprendizaje Automático (Machine Learning)__

El aprendizaje automático es una parte esencial del desarrollo de software. Ejemplos incluyen:
- Aceleración del análisis de imágenes astronómicas en un factor de 10 millones.
- Reducción del consumo energético en centros de datos en un 40%.
- Mejora de arquitecturas de computación según Google AI.

__Formas de Aprendizaje__

https://www.youtube.com/watch?v=oT3arRRB2Cw

- __Aprendizaje supervisado__: El agente aprende a partir de ejemplos etiquetados (ej. reconocer peatones en imágenes).
- __Aprendizaje no supervisado__: Encuentra patrones sin etiquetas explícitas (ej. agrupar imágenes similares).
- __Aprendizaje por refuerzo__: Aprende de recompensas y castigos (ej. mejorar su estrategia en ajedrez).

__Inducción vs. Deducción__
La inducción generaliza a partir de datos (ej. "el sol siempre ha salido, lo hará mañana"), pero no garantiza certeza, a diferencia de la deducción lógica.

https://www.youtube.com/watch?v=yKCmn7utNRc&t=426s

__Modelos de Aprendizaje__
El aprendizaje puede manejar datos representados como vectores de atributos (factored), estructuras atómicas o modelos relacionales. Según la naturaleza de la salida, el problema puede clasificarse como:

- Clasificación: Predicción de valores discretos (ej. soleado/lluvioso).
- Regresión: Predicción de valores numéricos (ej. temperatura del día siguiente).

Este capítulo sienta las bases para entender cómo los agentes pueden aprender y mejorar su rendimiento a partir de la experiencia.

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










