### Seleccion de características

En función de su noción de relevancia, una técnica de selección de características formula matemáticamente un criterio para evaluar el conjunto de características generadas.

¿Cómo se define la relevancia de una característica?

- Una característica "S" se condiera relevante si la eliminación de "S" deteriora el rendimiento de un clasificador
- La importancia de las características se mide con la correlación que presentan entre ellas.
- Una caracterísitca es relevante si es parte de un árbol de decisiones durante el proceso de clasificación.

## Importancia de la selección 

- __Reduce la dimensionalidad__ del conjunto de datos y ayuda a __mejorar el rendimiento__ de los algoritmos.

- __Mejora la calidad de los datos__ eliminando datos redundantes, irrelevantes o ruidosos.

- Mejora la precisión del modelo resultante.

- __Ayuda en la compresión de datos__, permitiendo, entre otras cosas, visualizarlos en gráficas de dos y tres dimensiones.

## Metodos de selección

- Valores perdidos: encontrar características con una fracción de valores perdidos por encima de un umbral especificado

- Valores únicos: Encontrar cualquier característica que tenga un solo valor único.

- Características colineales (altamente correlacionadas): Este método encuentra pares de características colineales basadas en el coeficiente de correlación de Pearson. Para cada par por encima del umbral especificado, identifica una de las variables que se eliminarán. Requiere un umbral de correlación.

- Características con cero importancia: Este método se basa en un modelo de aprendizaje automático para identificar las características que se eliminarán.



