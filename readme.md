## README

#### Pre-requisitos
Instalar mongodb o ejecutar una imagen de mongodb en docker.
Tener una base de datos mongodb. Llamarla: "quality" y crear la coleccion "testings"

#### Configuracion
Codigo ETL. Modificar las **rutas de las carpetas** "in" y "out" y el **string de conexion** a la base de datos mongoDB.
```python
#==============================================================
#RUTA DE LOS FICHEROS
path=".\in"
path_end=".\out"
#CARPETAS DE INSPECCION y CONFIGURACION
carpetas=[
  {"carpeta":"Moog","lineas":2,"delimitador":",","sepdecimal":'.'},
  {"carpeta":"Hoytom","lineas":0,"delimitador":'\t',"sepdecimal":','},
  {"carpeta":"Weiss","lineas":[0,1,2,3,4,6,7],"delimitador":";","sepdecimal":'.'}
]
#CONNECTION STRING A MONGODB
connectionString = "mongodb://localhost:30000,localhost:30001,localhost:30002/?replicaSet=rs0"
databasename="quality"
collectionname="testings"
#==============================================================

```
Tener instalado node.js para poder ejecutar el comando: node server.js