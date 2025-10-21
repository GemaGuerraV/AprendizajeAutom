## Tarea #4
### Universidad de Ciencias Físico Matemáticas
#### Maestría en Ciencia de Datos - Aprendizaje Automático

Para visualizar mi código en Collab da click [aquí](https://colab.research.google.com/drive/1TiLeFIIZq373IfFzPS1Fl1g8C8WAHgIZ?usp=sharing)

# Métricas para seleccionar características en literatura

-Eliminación recursiva de características con validación cruzada

Es un método de selección de características de tipo envoltura (wrapper).
La Eliminación Recursiva de Características (RFE) es un algoritmo de selección de características que se utiliza para seleccionar un subconjunto de las características más relevantes de un conjunto de datos. Es un proceso recursivo que comienza con todas las características del conjunto de datos y luego elimina iterativamente las menos esenciales hasta alcanzar el número deseado.
RFE utiliza un modelo (como una regresión lineal o una máquina de vectores de soporte ) para evaluar la importancia de cada característica, y las de menor importancia se eliminan en cada iteración.

Existen varios tipos de técnicas de validación cruzada , pero la más común es la validación cruzada de k-fold. En esta última, el conjunto de datos se divide aleatoriamente en k subconjuntos de igual tamaño. El modelo se entrena con k-1 subconjuntos y luego se prueba con el subconjunto restante. Este proceso se repite k veces, utilizando un subconjunto diferente como conjunto de prueba en cada iteración. El rendimiento del modelo se promedia a lo largo de las k iteraciones y se usan distintos métricos (F1-score, $R^2$)

# Carácteristicas más relevantes en mi BD
Considero que aplicando este método las características más relevantes para saber si un caballo ganó o no la carrera serán la edad, el peso, el tiempo entre secciones, el tiempo final, el tipo de piso de la carrera y las posibilidades de ganar. Esta consideración es debido a que el modelo rankea de menor a mayor importancia las variables y realiza una eliminación; Mi BD tiene varias variables que no agregan tanto valor al resultado. Este metodo sería bueno para mi conjunto de datos porque por medio de la validación de datos, mi modelo se entrena para tener una mejor predicción automática del resultado.

Fuentes:
GeeksforGeeks. Julio 2025. Recuperado de: https://www.geeksforgeeks.org/machine-learning/recursive-feature-elimination-with-cross-validation-in-scikit-learn/
