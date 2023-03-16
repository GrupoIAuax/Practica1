# Memoria Practica 1
En esta práctica hemos aprendido a utilizar varios métodos de web-scraping, también hemos aprendido a investigar y analizar como funciona una página de la cual queramos recolectar datos, para Wallapop estaremos usando su propia API mientras que para Filmaffinity haremos el scraping del propio html de la página.

A continuación explicamos detalladamente nuestro código.

# WALLAPOP
# 1. Parámetros
Creamos dos diccionarios llamados headers y params para establecer los argumentos que enviaremos con la petición a la API de Wallapop, esos parámetros especificaran por ejemplo el lugar y rango para la búsqueda, entre otros.


![Captura de pantalla 2023-03-14 220705](https://user-images.githubusercontent.com/98824525/225136974-836e1285-29df-4ef4-be17-b512218327a7.png)


# 2. Peticiones
Creamos una lista vacía llamada "listaDefinitiva" donde guardaremos los datos que recibamos. Los 4 objetos que buscaremos serán: Mancuernas, Skate, Piano, Raton; por lo tanto, hacemos que nuestro código haga una llamada a la API por cada uno de estos, la API nos responderá con un json por cada llamada y nosotros iremos almacenando la información que contenga.


![Captura de pantalla 2023-03-14 220903](https://user-images.githubusercontent.com/98824525/225137050-dfd038a9-e3c3-4086-942f-11d891701d16.png)


# 3. Filtramos 
A continuación recorreremos la listaDefinitiva para quedarnos solo con 4 parámetros de todo el contenido, que son:
- Título
- precio
- Descripción
- Imagenes


![Captura de pantalla 2023-03-14 220918](https://user-images.githubusercontent.com/98824525/225137173-927c6a65-e08f-46c9-a251-d769a10abd44.png)


# 4. Mostrar los objetos
Para ver los datos que hemos recolectado de forma más visual usaremos principalmente la librería display de Python, enseñaremos una muestra de cada 100 para ver varios ejemplos de los datos recolectados.


![Captura de pantalla 2023-03-14 220930](https://user-images.githubusercontent.com/98824525/225137261-1f75dbc4-35d0-41f6-b7d3-09eedc0a4b57.png)


Y aquí están las muestras de nuestros datos:

## Skate

![Captura de pantalla 2023-03-14 221957](https://user-images.githubusercontent.com/98824525/225139103-c01a8f26-2bb6-42f3-abc6-5502421dc30c.png)

## Mancuernas

![Captura de pantalla 2023-03-14 222031](https://user-images.githubusercontent.com/98824525/225139129-c2351a25-4c59-4ca0-95f7-b88ba30b3bea.png)

## Piano

![Captura de pantalla 2023-03-14 222048](https://user-images.githubusercontent.com/98824525/225139154-d307886c-0c9c-4983-a173-befe2dd22bd4.png)

## Ratón

![Captura de pantalla 2023-03-14 222107](https://user-images.githubusercontent.com/98824525/225139184-cf820206-4e83-45dd-b8c5-5048c4299108.png)

# FILMAFFINITY

# 1. Obtener películas
En Filmaffinity nos encontramos con la siguiente problemática, existen listas de películas por género de las cuales queremos obtener la información, pero en estas listas no está dicha información, entonces debemos obtener los enlaces de donde se encuentren los datos que queremos los cuales serán los enlaces específicos de cada película.

Para scrapear los datos de Filmaffinity usaremos la librería BeautifulSoup, usaremos esta librería para recorrer el código html de dos urls las cuales están especificadas en el código, estas urls son listas de películas de cada uno de los géneros que vamos a buscar.

Analizando el código html de Filmaffinity podemos encontrar las etiquetas del contenido que nos interesa, por lo tanto, hacemos referencia a estas etiquetas en nuestro código para solo quedarnos con las urls de las demás películas.


![Captura de pantalla 2023-03-14 224802](https://user-images.githubusercontent.com/98824525/225147858-92af497f-b487-4999-9518-ccb2a1f16fa9.png)


# 2. Obtener y guardar datos
Ahora llamamos a todas las urls que hemos obtenido, y como previamente también hemos analizado la estructura html de estas páginas, sabemos qué contenido es el que queremos guardarnos gracias a conocer las etiquetas del mismo, esos datos los almacenamos en un json.


![Captura de pantalla 2023-03-14 224850](https://user-images.githubusercontent.com/98824525/225148011-c6b0f61b-729b-4d59-b402-94688d53cca4.png)


# 3. Mostrar películas
Por último accedemos al json para mostrar las películas y asegurar que hemos guardado los datos de forma correcta.


![Captura de pantalla 2023-03-14 225017](https://user-images.githubusercontent.com/98824525/225148312-31f67ff0-2460-4e58-83d3-b78c803b66e3.png)


# 4. Películas
## Terror

![Captura de pantalla 2023-03-14 225055](https://user-images.githubusercontent.com/98824525/225148423-f27e329e-06bb-4dc7-a7bb-006a94ea5c4b.png)

## Comedia

![Captura de pantalla 2023-03-14 225216](https://user-images.githubusercontent.com/98824525/225148631-bd50dc11-c118-4317-853c-85bfe5f8bd01.png)

# Inconvenientes

A Filmaffinity no le gusta el scraping 🥲

![Captura de pantalla (1)](https://user-images.githubusercontent.com/98824525/225151708-fddeb892-a793-496a-93ea-424485777dd8.png)

