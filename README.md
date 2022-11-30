# AprendizajeAutomatico

Hecho por Pedro Bereilh, María Calvo Torres y Gonzalo Valdez Casis

## Pasos a realizar 

- **Elegir el problema:** En nuestro caso decidimos buscar un dataset sobre información de los distintos modelos y características de distintos coches.

- **Identificar la fuente de datos:** Decidimos utilizar una fuente de datos en formato csv que contiene características sobre coches y sobre el país o continente de origen de cada uno.

![](/images/Data.png)

- **Identificar las características relevantes de los hechos:** En nuestro caso las características son varias como, por ejemplo, Modelo del coche, cilindrada, caballos y la característica más importante que es país o continente de origen que puede ser US, Japan o Europe. Posteriormente eliminaremos la característica de nombre para que sea más complicado para el modelo encontrar el país o continente de origen.

- **Obtener un fichero .arff:** Le pasamos el fichero csv a weka que podemos encontrar en la carpeta data y lo convertimos en un arff. 

- **Evaluar distintos algoritmos de aprendizaje automático con los datos obtenidos:** Evaluamos todos los algoritmos para nuestro dataSet de coches. El mejor resultado nos lo dio el Random Forest. Como podemos ver en la imagen siguiente, vemos el resultado del algoritmo que nos da un 87% de acierto. También podemos ver que ha acertado correctamente 354 de 406.

![](/images/ResultadoAlgoritmo.PNG)

![](/images/GraficoEUROPA.PNG)

![](/images/GraficoJAPAN.PNG)

![](/images/GraficoUS.PNG)


## Como ejecutar el programa 

Creamos el fichero jar que contendrá todo lo necesario para poder ejecutar el programa utilizando el siguiente comando: 

```
make jar
```

Utilizamos el siguiente comando para ejecutar el jar y recibir una respuesta

```
java -jar aprendizaje.jar
```
La query que estamos utilizando para que el modelo encuentre la solución es: 270,4,9700,6000,1834,190,71,?. Esta sentencia se encuentra en el fichero test.arff. 

El símbolo ? indica que ese es el campo que queremos que nos devuelva el resultado. Como vamos a poder ver a continuación el resultado es "Europe".  

Para comprobar otra consulta, podemos cambiar este fichero modificando la query con otros valores y así comprobar que el modelo te devuelve otro país de origen y así poder confirmar que funciona correctamente. 
 
La respuesta de la query debería dar: 

![](/images/result1.png)


## Algoritmo RandomForest

"El algoritmo Random Forest es una técnica de aprendizaje supervisado que genera múltiples árboles de decisión sobre un conjunto de datos de entrenamiento: los resultados obtenidos se combinan a fin de obtener un modelo único más robusto en comparación con los resultados de cada árbol por separado. Cada árbol se obtiene mediante un proceso de dos etapas:

- Se genera un número considerable de árboles de decisión con el conjunto de datos. Cada árbol contiene un subconjunto aleatorio de variables m (predictores) de forma que m < M (donde M = total de predictores).

- Cada árbol crece hasta su máxima extensión."

> _Espinosa-Zúñiga, Javier Jesús. “Aplicación De Algoritmos Random Forest y Xgboost En Una Base De Solicitudes De Tarjetas De Crédito.” Ingeniería, Investigación y Tecnología, Facultad De Ingeniería, UNAM._

Este ha sido el algoritmo que hemos utilizado para realizar el modelo. 


