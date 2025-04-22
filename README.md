# Comando-estelar-Actividad Evaluativa

## Descripción
- clase4.ipynb es el notebook en donde se implementan los primeros dos pasos de la actividad: Montar la base de datos en SQL utilizando un Servidor de Azure y entrenar un modelo usando dicha base de datos. Para la conexión hay que tener los datos en un archivo connection_details.json
- class4_deployer.ipynb es el notebook que despliega el servicio creado en la nube. Se encarga de cargar las respectivas credenciales de Microsoft Azure, registrar el modelo, crear el ambiente virtual y confirgurar el entorno de inferencia para así, desplegar el servicio realizado en la nube. Este código genera el archivo score.py y uri.json.
- Prueba_API.ipynb es el notebook que carga los datos de prueba y los formatea adecuadamente para posteriormente, contruir la API y enviarlos a ella, generando un request para obtener las predicciones utilizando el servicio desplegado.  

## Archivos necesarios
- connection_details.json tienen la siguiente forma: 
{
    "server": "server",
    "database": "database",
    "username": "username",
    "password": "password"
}
- id_conf_c4.json contiene el id de suscripción para la utilización del grupo de recursos respectivo para desplegar el servicio en la nube con Microsoft Azure.
- model_regression.pkl contiene almacenado el modelo de regresión entrenado en clase4.ipynb y utilizado en el servicio desplegado en la nube.
- datos_prueba.csv es la base de datos de prueba que es enviada a la API para generar predicciones. Esta base de datos debe seguir estricta y exactamente el mismo formato que la base de datos con la que se entrenó el modelo utilizado en el servicio. En nuestro caso, generamos una en la que todas las columnas "no numéricas" se encuentran vacías.

## Instrucciones
1.- Fork it
2.- Correr clase4.ipynb. (Es necesario tener los datos de conexión en un archivo connection_details.json)
3.- Correr class4_deployer.ipynb (Es necesario tener el id de suscripción en un archivo id_conf_c4.json y el modelo entrenado alamecenado en un archivo pickle model_regression.pkl)
4.- Correr Prueba_API.ipynb (Es necesario tener el scoring uri del servicio desplegado en un archivo uri.json)
5.- Para realizar predicciones con el modelo de regresión implementado es necesario correr la API construida en el archivo Prueba_API.ipynb. (Nota: Es necesario reemplazar el archivo "datos_prueba.csv" por los datos que se desee consultar y deben seguir estrictamente las características de formato).

## Especificaciones de Software mínimo:
MacOS Sonoma 14.3/ Windows 11 
RAM: 4 GB
Ancho de Banda: 10 Mbps

## Especificaciones para datos de consulta en la API

