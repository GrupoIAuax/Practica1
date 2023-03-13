# WALLAPOP
# 1. Definir diccionarios
Creamos dos diccionarios llamados headers y params para establecer las peticiones que queremos enviar, especificando entre otras cosas la provincia, la region, la ciudad... entre otros parametros.

![image](https://user-images.githubusercontent.com/113373670/224575219-492ffb45-bb20-4ea2-952e-69199dcab211.png)


# 2. Definir, realizar y almacenar las búsquedas
Creamos una lista vacía llamada "listaDefinitiva" donde guardaremos los resultados finales, también crearemos otra lista llamada búsquedas donde se podrá ver las 4 búsquedas que queremos realizar en wallapop y obtener todas las existencias de las mismas.

Por último se realiza un bucle para cada búsqueda de la lista, realizaremos un cambio en el parámetro "keyboard" dentro del diccionario params para que se vaya actualizando su valor a las 4 búsquedas que solicitamos. Después de cumplir los requisitos de peticiones a la api de wallapop almacenaremos las respuestas en listaDefinitiva.

![image](https://user-images.githubusercontent.com/113373670/224575603-cfea589a-b106-4ef7-b77e-b52c4aef0e81.png)

# 3. Filtramos 
Ahora mediante un bucle recorriendo la listaDefinitiva queremos establecer que solo queremos 4 parámetros de todo el contenido, que son:
- Título
- precio
- Descripción
- Imagenes

![image](https://user-images.githubusercontent.com/113373670/224576619-4da41136-d368-4829-a6a0-58712283005f.png)

# 4. Mostrar los objetos

Mediante un bucle buscaremos un objeto entre 100 mostrando el título, precio y descripción para poder confirmar que encontramos las búsquedas.

![image](https://user-images.githubusercontent.com/113373670/224577295-b05c00e4-6d8b-499b-a621-09d75c3a5d1b.png)


# 5. Imágenes
Comprobamos que funciona.

## Skate

![image](https://user-images.githubusercontent.com/113373670/224577388-fbfaf99f-baf2-430f-a897-2d95e2563ba5.png)

## Mancuernas

![image](https://user-images.githubusercontent.com/113373670/224577434-fcbddedb-fef9-4adc-9968-57bd6f742dd8.png)

## Piano

![image](https://user-images.githubusercontent.com/113373670/224577459-2f2f05c7-1833-4162-b129-f37dc928a891.png)

## Ratón

![image](https://user-images.githubusercontent.com/113373670/224577479-811da595-64fd-412a-962d-ef2fe39015b2.png)

# FILMAFFINITY

# 1. Crear listas, almacenar y parsear

Creamos una lista llamada urls donde almacenamos las dos urls de de terror y comedia.
Realizamos un for para parsear el html y vamos a guardar todos los links de las películas que obtenemos a la lista movie_links.
Creamos un txt para guardar los links de las películas

![image](https://user-images.githubusercontent.com/113373670/224581103-cb4486dd-4cea-471e-ad1a-9f9099b21f41.png)

# 2. Filtrar las películas obtenidas

Abrimos el txt que creamos previamente y mediante un for filtramos y extraemos solo:
- Título
- Género
- Sinopsis

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

