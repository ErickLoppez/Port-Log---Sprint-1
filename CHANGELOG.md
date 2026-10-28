# CHANGELOG

## Sprint 3

[Ejercicio 07]

- Se creó la base de datos vectorial `buque_vectorial` con ChromaDB.
- Se cargó el modelo OpenCLIP para generar embeddings de imágenes.
- Se seleccionó una imagen `complete` por buque, conservando la de mayor ratio de coincidencia cuando había más de una.
- Se utilizaron las matrículas de los buques como identificadores en la colección vectorial.
- Se generaron y almacenaron embeddings para 16 buques con imagen `complete` asociada.
- Se validó una cobertura vectorial del 80.00% respecto de los 20 buques de la base relacional.


[Ejercicio 06]

- Se implementaron consultas SQLAlchemy sobre la base de datos relacional.
- Se obtuvo el top 10 de buques con mayor cantidad de infracciones.
- Se identificaron los 10 movimientos más recientes sin evidencia asociada.
- Se analizaron los radares más activos y la cantidad de muelles distintos en los que operaron.
- Se obtuvo el top 10 de buques reincidentes durante el período 2024-01-01 a 2024-12-31.
- Se calculó el exceso promedio de velocidad por muelle.
- Se calculó la cobertura de evidencia visual sobre el total de infracciones.
- La cobertura visual obtenida fue de 93 infracciones con imagen sobre 474 totales, equivalente al 19.62%.


[Ejercicio 05]

- Se creó la base de datos `transito_portuario` con SQLAlchemy.
- Se generaron automáticamente las tablas del modelo relacional.
- Se migraron los datos desde `port_movements_image.csv` utilizando `procesar_fila_csv`.
- Se preservaron los movimientos sin radar informado mediante el identificador técnico `SIN-DATO`.
- Se validaron 20 buques, 9 radares, 474 movimientos y 93 evidencias.


[Ejercicio 04]

- Se implementó el modelo relacional con SQLAlchemy.
- Se definieron las entidades Buque, Radar, Movimiento y Evidencia.
- Se incorporaron claves primarias, claves foráneas y relaciones con `relationship`.
- Se agregaron métodos `__repr__` para mejorar la legibilidad de las instancias.
- Se implementó la función `procesar_fila_csv`.
- Se validó correctamente la relación entre movimiento, buque, radar y evidencia.
- Se contempló el radar como dispositivo móvil, asociando el muelle al movimiento.


[Ejercicio 03]

- Se diseñó el modelo lógico a partir de `port_movements_image.csv`.
- Se definieron las entidades Buque, Movimiento, Radar y Evidencia.
- Se establecieron los atributos y cardinalidades del modelo.
- Se consideró que un radar puede registrar movimientos en distintos muelles.


[Ejercicio 02]

- Se inicializó DVC en el repositorio.
- Se configuró Supabase como almacenamiento remoto S3 para DVC.
- Se migró `data/raw/imgs` desde Git hacia DVC.
- Se generó `data/raw/imgs.dvc` y se actualizó el archivo `.gitignore`.
- Se enviaron correctamente las imágenes al almacenamiento remoto configurado en Supabase.
- Se migró `data/interim/plots` desde Git hacia DVC.
- Se generó `data/interim/plots.dvc` y se actualizó `data/interim/.gitignore`.
- Se enviaron correctamente los plots al almacenamiento remoto configurado en Supabase.
- Se migró `data/processed/port_movements_image.csv` desde Git hacia DVC.
- Se generó `data/processed/port_movements_image.csv.dvc` y se actualizó `data/processed/.gitignore`.
- Se envió correctamente el dataset procesado al almacenamiento remoto configurado en Supabase.
- Se versionó el dataset procesado con DVC para mantener la trazabilidad de las versiones de datos sin almacenar directamente cada versión completa en Git.

[Ejercicio 01]

- Se creó la rama Sprint_3 a partir de Sprint_2.
- Se verificó el acceso a los datasets generados en sprints anteriores.
- Se contabilizaron los registros de cada dataset.
- Se informó la fecha de última modificación de cada archivo.
- Se actualizó el README para el Sprint 3.

## Sprint 2

[Ejercicio 06]

- Se calculó el porcentaje de infracciones con evidencia visual válida.
- Se analizaron los resultados obtenidos mediante OCR.
- Se comparó la utilidad de los grupos plates y completes.
- Se analizaron las condiciones que afectan el reconocimiento de matrículas.
- Se propusieron mejoras para la captura y asociación de imágenes.

[Ejercicio 05]

- Se contabilizaron las infracciones con y sin imagen asociada.
- Se determinaron las imágenes sin coincidencia en el dataset.
- Se calculó el ratio promedio de las coincidencias encontradas.
- Se comparó la tasa de coincidencias de los grupos plates y completes.
- Se identificaron las infracciones PENDIENTE sin imagen asociada.

[Ejercicio 04]

- Se aplicó EasyOCR sobre las imágenes originales.
- Se almacenó el texto detectado en matricula_imagen.
- Se normalizaron las matrículas conservando solo caracteres alfanuméricos.
- Se implementó una comparación por posición con umbral mínimo del 75 %.
- Se asociaron las imágenes con las infracciones correspondientes.
- Se actualizó group_images.json con los resultados de OCR.
- Se generó data/processed/port_movements_image.csv.

[Ejercicio 03]

- Se convirtieron las imágenes originales a escala de grises.
- Se aplicó ecualización de histograma para mejorar el contraste.
- Se aplicó suavizado gaussiano para reducir ruido.
- Se aplicó detección de bordes mediante Canny.
- Se visualizaron muestras de los resultados obtenidos en cada etapa.

[Ejercicio 02]

- Se listaron las imágenes disponibles junto con su tamaño en KB.
- Se separaron las imágenes en los grupos plates y completes.
- Se construyó el diccionario group_images con los metadatos de cada imagen.
- Se exportó group_images en data/interim/group_images.json.
- Se calcularon resolución, área y tamaño promedio para cada grupo.
- Se implementó la función mostrar_muestra para visualizar imágenes aleatorias.

[Ejercicio 01]

- Se creó la rama Sprint_2 a partir de Sprint_1.
- Se descargó y descomprimió el dataset de imágenes.
- Se almacenaron las imágenes en data/raw/imgs.
- Se verificó la disponibilidad de los archivos generados en Sprint 1.
- Se contabilizaron los registros de los archivos heredados.

## Sprint 1

[Ejercicio 07]

- Se redactó la conclusión final del Sprint 1.
- Se evaluó la calidad del dataset heredado.
- Se resumieron los principales patrones de infracción.
- Se analizó el impacto de incorporar datos sin limpieza previa.
- Se propusieron mejoras para el proceso de captura de datos.
- Se exportó la conclusión en `reports/conclusion.md`.

[Ejercicio 06]

- Se calculó el porcentaje de infracciones con fecha inválida.
- Se calculó el porcentaje de infracciones con hora inválida.
- Se identificó el tipo de carga más frecuente entre las infracciones.
- Se identificó el origen más frecuente entre los buques infractores.
- Se calculó la duración promedio de estadía de los buques infractores.

[Ejercicio 05]

- Se generó el gráfico de las 10 matrículas más reincidentes.
- Se generó el gráfico de infracciones por turno.
- Se generó el gráfico de infracciones por mes.
- Se generó el histograma del exceso de velocidad real con curva KDE.
- Se generó el gráfico de exceso promedio por muelle.
- Se generó la comparación entre fechas válidas e inválidas.
- Se exportaron los gráficos en formato JPG.

[Ejercicio 04]

- Se definió la clase `PortAnalyzer`.
- Se encapsuló el DataFrame limpio.
- Se implementaron métodos para analizar infractores, turnos, excesos de velocidad, muelles y tipos de carga.
- Se creó una instancia de la clase y se ejecutaron todos los métodos solicitados.

[Ejercicio 03]

- Se normalizaron fechas y horas.
- Se calculó la duración de estadía.
- Se normalizaron matrículas y muelles.
- Se eliminaron filas con nulos en columnas críticas.
- Se detectaron y eliminaron outliers mediante IQR.
- Se calcularon los excesos de velocidad.
- Se eliminaron los registros sin infracción.
- Se exportó el dataset limpio y el resumen estadístico.

[Ejercicio 02]

- Se descargó y almacenó el dataset original.
- Se realizó una inspección inicial de los registros.
- Se analizaron los tipos de datos.
- Se contabilizaron los valores nulos.
- Se evaluó el porcentaje de valores correctos por columna.

[Ejercicio 01]

- Se inicializó y configuró Git.
- Se creó la rama Sprint_1.
- Se creó la estructura de directorios del proyecto.
- Se creó el archivo README.md.
- Se creó el archivo CHANGELOG.md.
