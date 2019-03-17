### Diferencia entre Gradient Boosting y Extreme Gradient Boosting Classifier

#### Gradient Boosting Classifier
Es un algoritmo de ‘ensemble learner’ que usa las técnicas de ‘boosting’ y ‘gradiente’ para entrenar modelos de manera gradual, aditiva y secuencial permitiendo optimizar(minimizando) y evaluar funciones de costo diferentes; esta función es una medida de cuán equivocado está el modelo en términos de su capacidad para estimar la relación entre X y y, entonces con el descenso del gradiente permite encontrar la dirección en la que se cambian los parámetros del modelo para reducir el error en la siguiente ronda de entrenamiento.  
En este modelo se emplea unos parámetros similares a Random Forests como: el número de iteraciones o estimadores (es decir, el número de árboles a ensamblar), el número de observaciones en cada hoja, complejidad y profundidad del árbol, la proporción de muestras y la proporción de características (variables) con las que se entrenan y se evalúan en cada split.  
Como se aplica el descenso del gradiente, los parámetros que o caracterizan y complementa a los anteriores mencionados son: la tasa de aprendizaje (realizando la analogía cuando se baja de una montaña para llegar al valle, este es el ‘tamaño del paso’, con un paso corto necesitas más pasos, con un paso largo puedes desviar la llegada al valle), la contracción (reducción de la tasa de aprendizaje) y la función de costo.  
#### Extreme Gradient Boosting Classifier
Se basa en el método Gradient Boosting con mejoras como:  
- Penalización o regularización avanzada (L1 y L2): hace que el algoritmo se mucho más potente y robusto porque mejora la generalización del modelo; estos parámetros de regularización estándar controlan el tamaño del árbol y la magnitud de los pesos en los nodos hoja.  
- Newton Boosting: métodos de aproximación donde se calculan segundas derivadas parciales (gradientes de segundo orden) que proporcionan más información o una ruta directa para llegar al mínimo de la función de costo para minimizar los errores de los estimadores y por ende del modelo general.   
- Computacionalmente proporciona: ejecución en palarelo y distribuido por las estructuras de los grandes datos para entrenar el modelo.  

Se concluye entonces que **XGBoost** emplea regularización para controlar el ajuste excesivo, las segundas derivadas para mayor rapidez de búsqueda de la minimización de la función de coste y fue diseñado para la eficiencia del tiempo de cómputo y los recursos de memoria, lo que brinda un mejor rendimiento y clasificación.

Basado en:
- https://medium.com/@gabrieltseng/gradient-boosting-and-xgboost-c306c1bcfaf5
- https://towardsdatascience.com/understanding-gradient-boosting-machines-9be756fe76ab
- https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/
- https://hackernoon.com/gradient-boosting-and-xgboost-90862daa6c77
- https://subscription.packtpub.com/book/big_data_and_business_intelligence/9781788295758/4/ch04lvl1sec34/comparison-between-adaboosting-versus-gradient-boosting
