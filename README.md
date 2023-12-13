# Predicción del consumo eléctrico de dispositivos IoT en el Edge Computing

## Preprocesado de datos (analisis_datos.ipynb)
En este archivo se hace un análisis exploratorio de los datoscon las siguientes tareas: 
 
* Identificar valores atípicos
* Segmentación de datos a partir de los intervalos de tiempo entre ellos
* Interpolación de nuevos datos a partir de los intervalos de tiempo entre ellos
* Normalizar los datos

## LSTM (lstm.ipynb)
Creación de un modelo basado en LSTM para resoluciones de 6h, 12h y 24h.

## CNN (cnn.ipynb)
Creación de un modelo basado en CNN para resoluciones de 6h, 12h y 24h.

## environmental_sensor_data/
Directorio con los datos en bruto (formato .csv).

## pickles/
Directorio donde se guardan los datos procesados y modelos para su posible carga posterior.

## resultados/
Directorio con capturas y logs de los resultados de los modelos.