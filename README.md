# Memoria Practica 1
En esta práctica hemos aprendido a utilizar varios métodos de web-scraping, también hemos aprendido a investigar y analizar como funciona una página de la cual queramos recolectar datos, para Wallapop estaremos usando su propia API mientras que para Filmaffinity haremos el scraping del propio html de la página.

A continuación explicamos detalladamente nuestro código.

# WALLAPOP
# 1. Parámetros
Creamos dos diccionarios llamados headers y params para establecer los argumentos que enviaremos con la petición a la API de Wallapop, esos parámetros especificaran por ejemplo el lugar y rango para la búsqueda, entre otros.


![image](https://user-images.githubusercontent.com/113373670/224575219-492ffb45-bb20-4ea2-952e-69199dcab211.png)


# 2. Peticiones
Creamos una lista vacía llamada "listaDefinitiva" donde guardaremos los datos que recibamos. Los 4 objetos que buscaremos serán: Mancuernas, Skate, Piano, Raton; por lo tanto, hacemos que nuestro código haga una llamada a la API por cada uno de estos, la API nos responderá con un json por cada llamada y nosotros iremos almacenando la información que contenga.

![image](https://user-images.githubusercontent.com/113373670/224575603-cfea589a-b106-4ef7-b77e-b52c4aef0e81.png)

# 3. Filtramos 
A continuación recorreremos la listaDefinitiva para quedarnos solo con 4 parámetros de todo el contenido, que son:
- Título
- precio
- Descripción
- Imagenes

![image](https://user-images.githubusercontent.com/113373670/224576619-4da41136-d368-4829-a6a0-58712283005f.png)

# 4. Mostrar los objetos

Para ver los datos que hemos recolectado de forma más visual usaremos principalmente la librería display de Python, enseñaremos una muestra de cada 100 para ver varios ejemplos de los datos recolectados.

![image](https://user-images.githubusercontent.com/113373670/224577295-b05c00e4-6d8b-499b-a621-09d75c3a5d1b.png)

Y aquí están las muestras de nuestros datos:

## Skate

![image](https://user-images.githubusercontent.com/113373670/224577388-fbfaf99f-baf2-430f-a897-2d95e2563ba5.png)

## Mancuernas

![image](https://user-images.githubusercontent.com/113373670/224577434-fcbddedb-fef9-4adc-9968-57bd6f742dd8.png)

## Piano

![image](https://user-images.githubusercontent.com/113373670/224577459-2f2f05c7-1833-4162-b129-f37dc928a891.png)

## Ratón

![image](https://user-images.githubusercontent.com/113373670/224577479-811da595-64fd-412a-962d-ef2fe39015b2.png)

# FILMAFFINITY

# 1. Obtener peliculas

En Filmaffinity nos encontramos con la siguiente problematica, existen listas de peliculas por genero de las cuales queremos obtener la informacion, pero en estas listas no esta dicha informacion, entonces debemos obtener los enlaces de donde se encuentren los datos que queremos los cuales seran los enlaces especificos de cada pelicula.

Para scrapear los datos de Filmaffinity usaremos la libreria BeautifulSoup, usaremos esta libreria para recorrer el codigo html de dos urls las cuales estan especificadas en el codigo, estas urls son listas de peliculas de cada uno de los generos que vamos a buscar.

Analizando el codigo html de Filmaffinity podemos encontrar las etiquetas del contenido que nos interesa, por lo tanto hacemos referencia a estas etiquetas en nuestro codigo para solo quedarnos con las urls de las demas peliculas.

![image](https://user-images.githubusercontent.com/113373670/224581103-cb4486dd-4cea-471e-ad1a-9f9099b21f41.png)

# 2. Obtener datos

Ahora llamamos a todas las urls que hemos obtenido, y como previamente tambien hemos analizado la estructura html de estas pagina, sabemos que contenido es el que queremos guardarnos gracias a conocer las etiquetas del mismo

![image](https://user-images.githubusercontent.com/113373670/224584898-3d3cd304-4ba2-4b82-a01d-45502140b783.png)

# 3. Guardamos en .JSON

Una vez ya obtenido las películas de terror y comedia, filtrar su contenido en función de lo que se nos pedía solo falta guardar el contenido en un .JSON y
mostrar las películas para asegurar que funciona de forma correcta por pantalla

![image](https://user-images.githubusercontent.com/113373670/224585146-0490a242-ce31-4e38-92fd-13c3ce9c0155.png)

# 4. Películas

## Terror
![image](https://user-images.githubusercontent.com/113373670/224585375-8cc233e6-36c2-4cb5-9560-e253b2212623.png)

## Comedia
![image](https://user-images.githubusercontent.com/113373670/224585449-0678489e-ec4d-4f0a-b062-8bcc181f7e02.png)

