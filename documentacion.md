# Preprocesado de datos

Agrupamos los ficheros por sensor:

1. Cargamos un fichero y lo ordenamos por 'timestamp'
2. Redondeamos el 'timestamp' a minutos
3. Nos quedamos solo el primer registro en un minuto
4. Mezclamos el fichero con el anterior y ordenado
5. Calculamos la diferencia de tiempo entre los registros

**¿Como analizamos los datos si son bloques separados?** -> Se analizan y limpian por separado, solo nos interesa limpiar, lo demás se enchufa directamente al modelo.

**¿Que hacemos con los los huecos temporales?** -> Insertar hasta 2 nuevos, con la media o media interpolada

**¿Que hacemos con los registros con datos faltantes?** -> Ver correlaciones con battery, los que nada los descartaremos y los que si, predecimos según los demás?

Si < 9, lo eliminamos, si > 15 y < 30, interpolamos 1 o 2, si > 30, split

Revisar si se ha hecho bien

Si tenemos

0 - 10 - 20 - 30 - 40- 50 - 60
0 -  15
0 -         26


Nans y -1, poner nans a -1 o interpolar.

Se puede interpolar antes de pasar a red neuronal, hay 10 min de margen