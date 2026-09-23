# Conclusión

El análisis del dataset heredado permitió detectar múltiples problemas de calidad de datos. De los 1500 registros originales se descartaron 1026, lo que representa un 68.40% del total. Entre los errores más frecuentes se encontraron horas inválidas, matrículas con formatos incorrectos, fechas inválidas, valores nulos en variables numéricas y registros con valores atípicos.

En relación con los patrones de infracción, el turno con mayor cantidad de casos fue por la Madrugada, con 134 infracciones. El muelle con mayor cantidad de infracciones fue MUELLE-D, con 87 registros. Además, el tipo de carga más frecuente entre los infractores fue el de CONTENEDORES, representando el 14.98% del total de infracciones.

También se observó que el 2.74% de las infracciones provenía de registros con fecha inválida y el 15.40% de registros con alguna hora inválida. La duración promedio de estadía de los buques infractores fue de 30.47 horas.

La incorporación directa de estos datos al nuevo sistema, sin una etapa previa de limpieza y validación, podría generar errores en los cálculos, clasificaciones incorrectas de infracciones y dificultades para realizar análisis confiables. También podría provocar que datos inconsistentes del sistema anterior continúen afectando el funcionamiento del nuevo sistema.

Propuesta de mejora, se recomienda incorporar validaciones automáticas durante la carga de datos. Las fechas y horas deberían validarse antes de ser almacenadas, las matrículas y muelles deberían utilizar formatos predefinidos y los campos numéricos deberían contar con rangos permitidos. También sería conveniente utilizar listas de opciones para variables categóricas como tipo de carga, muelle y estado del despacho, reduciendo así los errores de escritura manual.