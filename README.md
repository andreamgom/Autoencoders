# Autoencoders

## Introducción
Este proyecto se centra en el desarrollo y la implementación de un modelo de autoencoder para el procesamiento de imágenes. El objetivo principal es transformar imágenes de entrada de tamaño 14x14 a 28x28 y de 28x28 a 56x56.

## Autoencoder
Un autoencoder es una red neuronal artificial utilizada para el aprendizaje no supervisado de codificaciones eficientes. La idea principal detrás de un autoencoder es que se entrena para copiar su entrada a su salida. Internamente, tiene una capa oculta, que se utiliza para representar la entrada.

## Estructura del Modelo
El modelo de autoencoder en este proyecto consta de dos partes principales: el encoder y el decoder.

### Encoder
El encoder es responsable de comprimir la entrada en un espacio latente de menor dimensión. En este proyecto, el encoder es una red convolucional que consta de tres capas convolucionales, cada una seguida por una función de activación ReLU.

### Decoder
El decoder toma la salida del encoder (el "código") y la reconstruye para que coincida con la dimensión de la imagen original. Al igual que el encoder, el decoder en este proyecto es una red convolucional, pero utiliza convoluciones transpuestas para aumentar la dimensión de las imágenes.

## Superresolución
Además del autoencoder, este proyecto también implementa un modelo de superresolución. Este modelo utiliza una estructura similar a la del autoencoder, pero está diseñado específicamente para aumentar la resolución de las imágenes de entrada. En este caso, el modelo de superresolución puede tomar imágenes de 14x14 y generar imágenes de 28x28, y tomar imágenes de 28x28 para generar imágenes de 56x56.

## Entrenamiento del Modelo
El modelo se entrena utilizando una función de pérdida de error cuadrático medio (MSE) y un optimizador Adam. Durante el entrenamiento, el modelo intenta minimizar la diferencia entre las imágenes de entrada y las imágenes reconstruidas, lo que resulta en un modelo que puede generar reconstrucciones precisas de las imágenes de entrada.

## Resultados
Después del entrenamiento, el modelo puede tomar una imagen de entrada de 14x14 o 28x28 y generar una imagen de salida de 28x28 o 56x56, respectivamente. Aunque hay alguna pérdida de calidad debido al proceso de compresión y descompresión, el modelo es capaz de preservar las características principales de las imágenes de entrada en las imágenes de salida.

## Conclusión
Este proyecto demuestra la eficacia de los autoencoders y los modelos de superresolución para tareas de procesamiento de imágenes. Aunque el modelo actual tiene algunas limitaciones, como la pérdida de calidad en las imágenes reconstruidas, ha demostrado ser capaz de aumentar la resolución de las imágenes de entrada de manera efectiva.
