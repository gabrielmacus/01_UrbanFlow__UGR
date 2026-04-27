## Conclusiones
* Se pierden muchos datos debido a valores nulos en campos clave.
* Una parte considerable del dataset se pierde debido a no ser una infracción de tránsito.
* No se observan outliers con respecto a las velocidades medidas, por lo que podemos asumir que el radar está funcionando bien.
* Trabajar con datos placeholder en campos clave (como el de la fecha y hora) resulta en inconsistencias, se compromete la integridad de los datos.
* El no conocer los formatos de patentes válidos redunda en posibles infracciones inválidas por error de lectura.
