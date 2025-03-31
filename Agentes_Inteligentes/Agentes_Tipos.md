# Agentes Inteligentes

## Agentes y su entorno

Un agente es cualquier entidad capaz de percibir su entorno mediante sensores y actuar en él mediante actuadores. Los agentes pueden ser humanos (con ojos, oídos, manos, etc.) o robots (que reciben información de archivos, teclado o red y responden con mensajes, archivos o paquetes).

<img src="img/Agente.png" width="100">


![Agentes](img/Agente.png)


https://github.com/Cursos-Informatica/Inteligencia_Artificial/blob/main/Agentes_Inteligentes/img/Agente.png

El comportamiento de un agente se describe mediante su función de agente, que asigna una acción a cada secuencia de percepciones. Esta función puede representarse en una tabla, aunque generalmente es demasiado grande. Para agentes artificiales, esta función se implementa mediante un programa del agente en una arquitectura específica.

Como ejemplo, el mundo de la aspiradora tiene dos cuadrículas (A y B), donde la aspiradora percibe su ubicación y si hay suciedad. Un agente simple sigue la regla: si hay suciedad, aspirar; de lo contrario, moverse.

Finalmente, la noción de agente es una herramienta analítica más que una clasificación absoluta, ya que, en teoría, incluso una calculadora podría considerarse un agente..

## Comportamiento correcto: el concepto de racionalidad

Un agente racional es aquel que toma decisiones que maximizan su éxito según una medida de rendimiento definida por su diseñador. Su racionalidad depende de cuatro factores, cada uno con ejemplos:

- La medida de rendimiento (cómo se evalúa el éxito).

    Ejemplo: En el caso de una aspiradora autónoma, la medida de rendimiento podría ser la cantidad de suciedad eliminada en un periodo de tiempo. Si la métrica fuera solo "movimiento constante", la aspiradora podría moverse sin limpiar, lo que no sería realmente útil.

- Su conocimiento del entorno (qué sabe sobre su mundo).

    Ejemplo: Un coche autónomo que conoce el mapa de la ciudad puede anticipar rutas eficientes. Sin embargo, si no sabe que hay una calle cerrada, podría intentar tomar un camino bloqueado.

- Las acciones disponibles (qué puede hacer el agente).

    Ejemplo: Un dron de entrega puede solo avanzar, girar y aterrizar. Si necesita evitar un obstáculo y no puede retroceder, su falta de opciones podría llevarlo a quedarse atascado.

- La secuencia de percepciones recibidas (qué ha experimentado hasta ahora).

    Ejemplo: Un asistente de voz aprende de las palabras que ha escuchado. Si una persona habla en otro idioma y el asistente nunca ha recibido palabras en ese idioma, no podrá responder correctamente.

Un agente no necesita ser perfecto, sino actuar de manera que maximice el rendimiento esperado con la información disponible. No es lo mismo racionalidad que omnisciencia. Además, un agente debe ser autónomo y aprender de su experiencia para mejorar su desempeño con el tiempo. 

Ejemplo de la avispa cavadora:
La avispa cavadora tiene un comportamiento programado. Cuando captura una oruga para alimentar a sus crías, sigue un procedimiento fijo:

- Cava una madriguera.
- Trae la oruga y la deja en la entrada.
- Entra a revisar que todo esté bien.
- Si todo está bien, arrastra la oruga adentro.

Si alguien mueve la oruga unos centímetros mientras la avispa está dentro revisando, al salir repetirá el proceso desde el paso 2 en lugar de adaptarse. Este comportamiento muestra falta de aprendizaje y autonomía, ya que la avispa sigue el mismo procedimiento sin cuestionarlo.

## Construcción de Agentes Racionales y Entornos de Trabajo
Para diseñar agentes racionales, primero es necesario comprender los entornos en los que operan. Estos entornos representan los "problemas" que los agentes buscan resolver. Para ello, se define un marco de especificación conocido como REAS (Rendimiento, Entorno, Actuadores y Sensores).

### Especificación del Entorno de Trabajo
El entorno de trabajo de un agente debe definirse de manera clara para diseñarlo de forma efectiva. Un ejemplo introductorio es el agente aspiradora, donde se establecen los elementos clave de su entorno, como la presencia de suciedad y los movimientos del agente.

Un ejemplo más complejo es el de un taxista automatizado, cuyo entorno incluye múltiples variables:

| Tipo de agente | Medidas de rendimiento | Entorno       | Actuadores   | Sensores                     |
|----------------|------------------------|---------------|--------------|------------------------------|
|Taxista         | Seguro, rápido,legal,  | Carreteras,   | Dirección,   | Cámaras, sónar, velocímetro, |
|                | viaje confortable,     | otro tráfico, | acelerador,  | GPS, tacómetro, visualizador |
|                | maximización           | peatones,     | freno, señal,| de la aceleración, sensores  |
|                | del beneficio          | clientes      | bocina,      | del motor, teclado           |
|                |                        |               | visualizador |                              |


Este análisis muestra cómo la complejidad del entorno afecta el diseño del agente.

### Propiedades de los Entornos de Trabajo
Los entornos de trabajo pueden clasificarse según diversas dimensiones, lo que influye en el diseño de los agentes.

a) Totalmente observable vs. _Parcialmente observable_
- Un entorno es totalmente observable si el agente puede acceder a toda la información relevante en cada momento.
- Es parcialmente observable si existen factores desconocidos o sensores limitados (por ejemplo, un taxi no puede saber qué piensan otros conductores).

b) Determinista vs. _Estocástico_
- Un entorno es determinista si su estado futuro depende completamente del estado actual y de las acciones del agente.
- Es estocástico si existen elementos impredecibles (ej., el tráfico para un taxi).

c) Episódico vs. _Secuencial_
- Un entorno episódico implica que cada acción del agente es independiente de las anteriores (ej., un sistema de inspección en una fábrica).
- Un entorno secuencial requiere considerar acciones pasadas, ya que afectan el futuro (ej., un taxista tomando decisiones de ruta).

d) Estático vs. _Dinámico_
- Un entorno estático no cambia mientras el agente toma decisiones (ej., un crucigrama).
- Un entorno dinámico cambia constantemente y requiere que el agente se adapte en tiempo real (ej., el tráfico).

e) Discreto vs. _Continuo_
- Un entorno es discreto si tiene un número finito de estados y acciones (ej., ajedrez).
- Es continuo si sus estados y acciones varían sin límites definidos (ej., la conducción de un automóvil).

f) Agente individual vs. _Multiagente_
- Un entorno de agente individual implica que el agente interactúa solo con el medio (ej., un sistema de diagnóstico médico).
- Un entorno multiagente implica la interacción con otros agentes, que pueden ser competitivos (ajedrez) o cooperativos (evitar colisiones en tráfico).

### Complejidad y Simulación de Entornos
En la práctica, la mayoría de los entornos reales combinan múltiples dimensiones de complejidad, como ocurre con el taxi automatizado (parcialmente observable, estocástico, secuencial, dinámico, continuo y multiagente).

Para evaluar el desempeño de los agentes en diferentes entornos, se utilizan simuladores, los cuales pueden generar variaciones en las condiciones para probar su adaptabilidad.

En Conclusión, el diseño de un agente racional requiere una comprensión detallada de su entorno de trabajo. La clasificación de los entornos según sus propiedades ayuda a determinar qué estrategias y técnicas deben emplearse en la construcción del agente. Entornos más complejos requieren agentes más sofisticados, lo que influye directamente en la implementación de la inteligencia artificial.

## Tipos de Agentes en Inteligencia Artificial
### 1. Agentes Reactivos Simples
- Definición: Responden a las percepciones actuales sin considerar el historial.
- Ejemplo: Una aspiradora automática que decide limpiar solo si detecta suciedad.
- Funcionamiento: Se basa en reglas de condición-acción, como "si el coche de adelante frena, entonces frenar".
- Limitaciones:

    - No funcionan bien en entornos parcialmente observables.
    - Pueden caer en bucles infinitos.
    - La aleatoriedad puede mejorar su desempeño en ciertos casos, pero sigue siendo un enfoque limitado.

### 2. Agentes Reactivos Basados en Modelos
- Definición: Incorporan un estado interno para representar información sobre partes del mundo que no pueden ver directamente.
- Ejemplo: Un coche autónomo que recuerda la posición de otros vehículos aunque no los tenga a la vista.
- Funcionamiento:
    - Utilizan un modelo del mundo que representa cómo evolucionan los objetos y cómo afectan las acciones del agente.
    - Se combinan percepciones actuales con el estado interno para tomar decisiones más informadas.

### 3. Agentes Basados en Objetivos
- Definición: Además de percibir el mundo, tienen metas que guían sus decisiones.
- Ejemplo: Un taxi autónomo que decide si girar o seguir recto en función del destino del pasajero.
- Funcionamiento:
    - Evalúan diferentes acciones y sus consecuencias en función de los objetivos.
    - Requieren técnicas como búsqueda y planificación para encontrar secuencias de acciones óptimas.

- Ventajas:
    - Más flexibles que los agentes reactivos.
    - Permiten adaptaciones dinámicas (ej. ajustar el comportamiento según el clima).

### 4. Agentes Basados en Utilidad
- Definición: No solo buscan alcanzar metas, sino que optimizan la calidad de sus decisiones mediante una función de utilidad.
- Ejemplo: Un taxi que elige la ruta más rápida y segura en lugar de solo llegar al destino.
- Funcionamiento:
    - Usan una función de utilidad para cuantificar el valor de diferentes estados posibles.
    - Permiten tomar decisiones racionales al equilibrar diferentes factores (ej. rapidez vs. seguridad).

- Ventajas:
    - Pueden manejar situaciones con objetivos en conflicto.
    - Permiten decisiones óptimas incluso en entornos inciertos.

### 5. Agentes que Aprenden
- Definición: Son capaces de mejorar su desempeño a lo largo del tiempo mediante el aprendizaje.
- Ejemplo: Un programa de ajedrez que aprende de sus errores y mejora sus estrategias.
- Componentes:
    - Elemento de actuación: Ejecuta acciones basadas en percepciones.
    - Elemento de aprendizaje: Ajusta el comportamiento del agente para mejorar su desempeño.
    - Crítica: Evalúa el desempeño del agente y proporciona retroalimentación.
    - Generador de problemas: Explora nuevas estrategias para mejorar el aprendizaje.

Ventajas:
    - Pueden adaptarse a entornos desconocidos.
    - Mejoran con la experiencia, evitando la necesidad de programar todas las reglas manualmente.

