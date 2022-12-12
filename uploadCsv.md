# Upload del CSV

La subida del csv está manejado a través de HTTP a través del endpoint `/csv-upload`. En el body espera un `form-data` con los siguientes campos:
```
answersCSV: File
teachersCSV: File
semester: Text
year: Text
```

Dicho endpoint procesará uno a uno primero las respuestas, creando las entidades nuevas que vaya encontrando o bien actualizándolas. Luego, procesará el CSV de profesores para poder asociar su DNI.

En caso de algún error o discrepancia, deshará todo el proceso e informará del error encontrado.