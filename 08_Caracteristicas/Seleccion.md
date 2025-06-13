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

## Métodos de selección

- __Valores perdidos:__ encontrar características con una fracción de valores perdidos por encima de un umbral especificado

- __Valores únicos:__ Encontrar cualquier característica que tenga un solo valor único.

- __Características colineales (altamente correlacionadas):__ Este método encuentra pares de características colineales basadas en el coeficiente de correlación de Pearson. Para cada par por encima del umbral especificado, identifica una de las variables que se eliminarán. Requiere un umbral de correlación.

- __Características con cero importancia:__ Este método se basa en un modelo de aprendizaje automático para identificar las características que se eliminarán.

## Método de selección : Random Forests

- Se puede medir la importancia de una característica en función de como ha reducido la impureza de los nodos de un árbol de decisión.

- Random Forest es un buen método para obtener intuiciones de si una característica del conjunto de datos realmente es necesaria.

## Métodos de Extracción

Existen diversos métodos de extracción de características, dos de los más populares son:

- Principal Component Analysis - PCA: Reducción de dimensionalidad lineal usando descomposición del valor singular de los datos para proyectarlo a un espacio dimensional inferior.

- Singular Value Descomposition - SVD: Es un método de descomposición para reducir una matriz a sus partes constituyente con el fin de hacer ciertos cálculos posteriores de matrices más simples.

__Principal Component Analysis - PCA__

- Se selecciona el eje que minimiza la distancia medida como el error de cuadrados entre el conjunto de datos original y sus proyección.

- El vector que define el eje se conoce como __Componente Principal__


__Singular Value Descomposition -SVD__

- Permite descomponer la matriz que compone el conjunto de datos X en la multiplicación de tres matrices: U sumatoria V a la T

- La matriz V contiene los Componentes Principalesa que se utilizan en el algoritmo PCA.







