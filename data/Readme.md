## Conclusiones
* Se pierden muchos datos debido a valores nulos en campos clave.
* Una parte considerable del dataset se pierde debido a no ser una infracción de tránsito.
* No se observan outliers con respecto a las velocidades medidas, por lo que podemos asumir que el radar está funcionando bien.
* Trabajar con datos placeholder en campos clave (como el de la fecha y hora) resulta en inconsistencias, se compromete la integridad de los datos.
* El no conocer los formatos de patentes válidos redunda en posibles infracciones inválidas por error de lectura.

## Conclusiones Sprint 2
* Debido a las diferentes condiciones de captura de imágenes (iluminación variada, desgaste de la patente, calidad de la cámara, distancia de captura, región de la patente con distinto fondo/tipografía/logos, y ángulo de captura que genera deformación u oclusión parcial), utilizar visión artificial en el pipeline puede ser beneficioso para normalizar la imagen, pero no alcanza por sí solo para una aplicación productiva.
* Muchas veces la patente se funde visualmente con el vehículo, lo que dificulta enormemente la detección a través de tratamientos tradicionales de imagen como binarización y operaciones morfológicas.
* En lo que respecta al reconocimiento de caracteres, si bien estamos usando un modelo de IA, al ser generalista es difícil obtener un match exacto debido a las condiciones mencionadas.
* Para un entorno de producción, se sugiere usar un modelo que esté entrenado específicamente para la detección de patentes en el contexto de un vehículo (ya sea trompa o parte trasera) y el reconocimiento de caracteres especializado en recortes de chapas patentes.
