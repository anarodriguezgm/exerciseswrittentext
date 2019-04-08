
### Amazon Comprehend  
Más que un producto comercial, Amazon Comprehend es un servicio que ofrece procesamiento de lenguaje natural (NLP) para extraer información sobre el contenido de los documentos.Trabaja identificando lo siguiente:  
- Idioma: identifica el idioma dominante en un documento entre 100 idiomas, y se apoya en los identificadores de RFC 5646 para esta tarea, que consiste en una lista de tags o combinación de letras  denominados códigos de idioma que permiten identificar el lenguaje de un texto.
- Sintaxis: analiza cada palabra y determina la función de la palabra dentro de la oración, es decir si es un verbo,  nombre propio, de artículo, adverbio, entre otro. Utiliza las operaciones  DetectSyntax y BatchDetectSyntax que se basan en Universal POS tags con 17 categorías, luego entonces la operación devuelve tokens que identifican la palabra y la función que representa en el texto. 
- Entidades: una entidad es una referencia textual al nombre único de un objeto del mundo real, como personas, lugares y elementos comerciales, y a referencias precisas de medidas como fechas y cantidades. Aquí utiliza las operaciones DetectEntities , BatchDetectEntities y StartEntitiesDetectionJob para detectar entidades en un documento.
- Sentimiento: se entiende como el grado de positividad o negatividad del texto, emplea las operaciones DetectSentiment, BatchDetectSentiment, StartSentimentDetectionJob que básicamente retornan el sentimiento detectado y un score.
- Frases claves: una frase es cadena que describe una cosa en particular, la frase incluye una puntuación que indica el nivel de confianza que tiene Amazon Comprehend de que la cadena es una frase nominal y esta puntuación sirve para  determinar si la detección tiene la confianza suficiente para su aplicación. Emplea las funciones internamente creadas como 
- Tema: permite identificar mediante el contenido de un documento, el tema o incluso en varios documentos temas comunes. Aquí usa un modelo de aprendizaje basado en  Latent Dirichlet Allocation para determinar los temas en un conjunto de documentos. Examina cada documento para determinar el contexto y el significado de una palabra. El conjunto de palabras que frecuentemente pertenecen al mismo contexto en todo el conjunto de documentos conforman un tema.

Este servicio es completamente administrado por Amazon, no hay equipos de cómputo por aprovisionar ni modelos de machine learning que construir, entrenar ni implementar, todo está alojado.


Por: Ana Milena Rodríguez

Tomado de:  
https://aws.amazon.com/es/comprehend/
https://aws.amazon.com/es/comprehend/features/
https://docs.aws.amazon.com/es_es/comprehend/latest/dg/what-is.html
https://docs.aws.amazon.com/es_es/comprehend/latest/dg/how-it-works.html
https://docs.aws.amazon.com/es_es/comprehend/latest/dg/topic-modeling.html
http://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf
https://docs.aws.amazon.com/es_es/comprehend/latest/dg/how-entities.html
