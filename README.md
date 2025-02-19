# MovieAI
En este espacio esta el código creado por nuestro grupo 

# MovieAI

MovieAi es un chatbot desarrollado para recomendar películas de manera personalizada utilizando inteligencia artificial. Este proyecto utiliza técnicas avanzadas de procesamiento de lenguaje natural y redes neuronales para analizar descripciones y géneros de películas proporcionados por los usuarios.

## Tabla de contenidos

1. [Nombre](#Nombre)
2. [Descripción](#descripción)
3. [Arquitectura](#Arquitectura)
4. [Proceso](#Proceso)
5. [Funcionalidades](#Funcionalidades)
6. [Estado del proyecto](#EstadoDelProyecto)
7. [Agradecimientos](#Agradecimientos)


* MovieAI

* MovieAi sugiere opciones relevantes, transformando la búsqueda de películas en una experiencia rápida y precisa. Ideal para quienes buscan optimizar el tiempo y encontrar películas que se ajusten exactamente a sus preferencias en cualquier ocasión.
  ![WhatsApp Image 2024-07-11 at 11 02 47 AM](https://github.com/repositoriosHackaton/MovieAI/assets/149196071/8e035da7-615b-4ade-ab84-67ef7915e3f6)

* Arquitectura del proyecto (Imagen)

* Proceso de desarrollo:
* Fuente del data
  El dataset se carga desde un archivo JSON llamado movies.json. Este archivo contiene descripciones de películas y sus respectivas calificaciones.
  
-Limpieza de datos (Imagen)
  Tokenización: Las descripciones de las películas se tokenizan usando Tokenizer de Keras.
  , Padding: Las secuencias tokenizadas se rellenan (pad_sequences) para asegurar que todas tengan la misma longitud.
  , Escalado de Calificaciones: Las calificaciones se escalan entre 0 y 1 utilizando MinMaxScaler.
  
-Manejo excepciones/control errores
ValueError: Descripción: Esta excepción se lanza cuando una función recibe un argumento del tipo correcto pero con un valor inapropiado.
tf.errors.InvalidArgumentError: Descripción: Esta excepción específica de TensorFlow se lanza cuando se pasa un argumento inválido a una función de TensorFlow. Uso en el código: Para capturar errores de argumento inválido que pueden surgir durante la definición o compilación del modelo.

-¿Qué modelo de Machine Learning están usando?
  El modelo implementado es una red neuronal secuencial de Keras con las siguientes capas:
    Embedding
    , LSTM (Long Short-Term Memory)
    , GlobalMaxPooling1D
    , Dense (con activación ReLU)
    , Dense (con activación Sigmoid).

-Métrica(s) de evaluación del modelo
  Mean Absolute Error (MAE): La métrica principal utilizada para evaluar el modelo.
  , Mean Squared Error (MSE): La función de pérdida utilizada durante el entrenamiento.
  
* Funcionalidades extra:
  Librerías: numpy, tensorflow, sklearn
  , Framework: Keras (dentro de TensorFlow).
  
