# AprendizajeAutomatico

Hecho por Pedro Bereilh, María Calvo Torres y Gonzalo Valdez Casis

## Pasos a realizar 
- **Elegir el problema:** En nuestro caso decidimos buscar un dataset sobre información de coches sobre distintos modelos y características de cada uno. 
- **Identificar la fuente de datos:** Decidimos utilizar una fuente de datos que contenia características sobre coches y sobre el país de origen de cada uno.

![](/images/Data.png)

- **Identificar las características relevantes de los hechos:** En nuestro caso las características son varias como por ejemplo Modelo del coche, cilindrada, caballos y la característica mas importante que es pais de origen que puede ser US, Japan o Europe.
- **Obtener un fichero .arff:** Le pasamos el fichero csv a weka que podemos observar en la carpeta data y lo convertimos en un arff. 
- **Evaluar distintos algoritmos de aprendizaje automático con los datos obtenidos:** Evaluamos todos los algoritmos para estos datos de coches y el que mejor resultado nos dios es Random Forest. Como podemos ver en la imagen siguiente vemos el resultado del algoritmo que nos de un 87% de acierto acertando 339 de 406.

![](/images/)


## Como ejecutar el programa 

Creamos el fichero jar que contendra todo para poder ejecutar el programa

```
make jar
```

Usamos este comando para ejecutar el jar y recibir una respuesta

```
java -jar aprendizaje.jar
```

La query que estamos haciendo a ver si el modelo responde correctamente es lo que esta dentro del fichero test.arff que va a remplazar el valor ? por la respuesta que en este caso deberia ser Europe como vemos comentado al lado.

![](/images/query.png)

La respuesta deberia ser: 

![](/images/result.png)



