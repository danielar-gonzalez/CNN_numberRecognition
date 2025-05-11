# Reconocimiento de Dígitos del 0-9 utilizando Redes Neuronales Convolucionales (CNN)

Este proyecto implementa un sistema de reconocimiento de dígitos del 0 al 9 utilizando redes neuronales convolucionales (CNNs). El proceso comienza en el archivo _CNNmodels.ipynb_, donde se importan las imágenes necesarias para entrenar y validar el modelo. Debido a las restricciones de tamaño de archivo, las imágenes utilizadas no se incluyen en el repositorio; sin embargo, el sistema es completamente compatible con conjuntos de datos estándar como MNIST.

Inicialmente se entrena una CNN base. Con base en los resultados obtenidos en cuanto a precisión (accuracy), se realizan modificaciones estructurales a la red, generando un total de cinco nuevas arquitecturas CNN. Cada una de estas variantes se entrena y se evalúa utilizando un conjunto de validación. Posteriormente, se comparan los desempeños obtenidos por cada modelo y se selecciona como “modelo ganador” aquel que presente el mejor rendimiento.

Una vez seleccionada la arquitectura óptima, se entrena nuevamente una red CNN con esta configuración, pero ahora utilizando el conjunto completo de entrenamiento. El modelo final se evalúa con un conjunto de prueba, utilizando métricas como la precisión (accuracy) y la matriz de confusión para verificar su capacidad de generalización. Este modelo entrenado se guarda en el repositorio bajo el nombre _modelWin.h5_.

Adicionalmente, el repositorio incluye el archivo _liveTesting.ipynb_, en el cual se carga el modelo ganador para realizar reconocimiento de dígitos en tiempo real utilizando la cámara de la computadora. Esto permite detectar y clasificar números escritos a mano o impresos directamente desde el flujo de video.

También se incluye el archivo _OCRmodel.ipynb_, que extiende la funcionalidad del modelo anterior integrando técnicas de Reconocimiento Óptico de Caracteres (OCR). En este notebook se abre la cámara, se capturan imágenes y se identifica automáticamente la región o regiones en las que se encuentran uno o varios dígitos. Cada dígito es localizado y clasificado individualmente, permitiendo reconocer múltiples números en una sola imagen.

Este proyecto requiere Python 3 y bibliotecas como TensorFlow/Keras, OpenCV, NumPy y Matplotlib. 

**Documentos incluídos en este repositorio:**
- [Entrenamiento de los modelos y evaluación de los mismos](./CNNmodels.ipynb)
- [Modelo Ganador probado en Tiempo Real](./liveTesting.ipynb)
- [Modelo Ganador con OCR implementado](./OCRmodel.ipynb)
- [Modelo Ganador](./modelWin.h5)
