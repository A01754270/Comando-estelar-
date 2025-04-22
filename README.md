# Comando-estelar-Actividad Evaluativa

## Descripción
- clase4.ipynb es el notebook principal en donde se implementa la actividad. Incluyendo el servidor en Azure con la base de datos de prueba de SQL. Para la conexión hay que tener los datos en un archivo connection_details.json
- class4_deployer.ipynb es el notebook que despliega el servicio creado en la nube. Se encarga de cargar las respectivas credenciales de Microsoft Azure, registrar el modelo, crear el ambiente virtual y confirgurar el entorno de inferencia para así, desplegar el servicio realizado en la nube.
- Prueba_API.ipynb es el notebook que
- datos_prueba.csv es la base de datos de prueba utilizada en la API para generar predicciones. Todas las filas "no numéricas" contienen datos N

## Archivos necesarios
- connection_details.json tienen la siguiente forma: 
{
    "server": "server",
    "database": "database",
    "username": "username",
    "password": "password"
}
- id_conf_c4.json contiene el id de suscripción para la utilización del servicio de Microsoft Azure.

## Instrucciones
