# Lineamientos  imágenes,videos y documentos

Para las imágenes, videos y documentos usaremos la plataforma de [cloudinary](https://cloudinary.com/) 
como CDN y optimización de imágenes.

<!-- ![Alt text](../assets/img/view-cloudinary.png?raw=true "Cloudinary") -->

Para un mejor lineamiento  las imágenes, videos y documentos deben estar:

- En minúsculas.
- Sin tildes.
- Separado en guión(-) si el nombre lo requiere.
- Formatos de videos en mp4.
- Formatos de imágenes svg,png y jpg.

Nota: NO se aceptan estas formas de nombrar archivos.
  
  - MI_ARCHIVO$.pdf
  - Imagen_de_Presentación...50%DSC.jpg
  - Imagen_de_Presentación.PNG
  - mI_Video@-upc.MP4
  - NUEVO_Video@-upc100%.mp4

##### Estandares recomendados para imágenes y videos

Para imágenes

Calidad de imágen de 70 a 80

- Desktop 1600x(tamaño relativo)
- Mobile  720X(tamaño relativo)

Para Videos

- Formato mp4
- Full HD(1920 x 1080) 


#### Cloudinary

Al momento de acceder a la [plataforma](https://cloudinary.com/) seleccionar la pestaña de "Media Library"
se mostrara los repositorios de las páginas UPC inluido los Open Portals 
como se muestran en la imagen.

![Alt text](../assets/img/cloudinary1.png?raw=true "Cloudinary1")

Para agregar Imágenes y videos seleccionar la opción "Upload"

![Alt text](../assets/img/cloudinary-upload.png?raw=true "Cloudinary1")

##### Sólo para el caso de videos

Luego de subir el video seleccionar el icono cuadrado "Edit" para optimizar y sea compatible con todos los navegadores con la calidad recomendada.

![Alt text](../assets/img/edit-video.png?raw=true "Cloudinary1")

Y luego se mostrara la siguiente pantalla 

    1. Seleccionar en la sección Video codec -> "h264"
    2. Dar por teminado en el boton  "Done"


![Alt text](../assets/img/config-video.png?raw=true "Cloudinary1")



#### Estructuras 

Para imágenes globales como logos UPC o WASC 
- Los logos upc deben estar en formato svg (rojo y blanco).
- Las imágenes para redes sociales en formato png.

Para imágenes generales 

````text
img-globales/
|
|---
    |-- logos/
    |   |-- logo-upc-red.svg/
    |   |-- logo-upc-blanco.svg/
    |   
    |
    |-- redes-sociales/
        |-- facebook.png
        |-- instagram.png/
        |-- twitter.png/
  

````

Para Pregrado 

````text
pregrado/
|
|-- carreras/
|   |-- carrera-a/
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|
|-- facultades/
|   |-- facultad-a
|   |   |-- videos/
|   |   |-- images/
|   |   |-- doc/
|   |
|   |-- facultad-b
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|
|-- modalidades/
|   |-- modalidad-a
|   |   |-- videos/
|   |   |-- images/
|   |   |-- doc/
|   |
|   |-- modalidad-b
|       |-- videos/
|       |-- images/
|       |-- doc/
|
|   
|-- eventos/
|   |-- evento-a
|   |    |-- videos/
|   |    |-- images/
|   |    |-- doc/
|   |
|   |-- evento-b
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|
|-- OG/
    |-- img-para-metadata.jpg

````

Para EPE 

````text
epe/
|
|-- admision-epe/
|   |-- videos/
|   |-- images/
|   |-- doc/
|   
|
|-- carreras/
|   |-- carrera-a/
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|     
|-- eventos/
|   |-- evento-a
|   |    |-- videos/
|   |    |-- images/
|   |    |-- doc/
|   |
|   |-- evento-b
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|   
|
|-- OG/
    |-- img-para-metadata.jpg

````
Para Institucional 

````text
institucional/
|
|-- directorio/
|   |-- videos/
|   |-- images/
|   |-- doc/
|   
|
|-- noticias/
|   |-- carrera-a/
|       |-- videos/
|       |-- images/
|       |-- doc/
|
|-- internas/
|   |-- interna-a/
|   |   |-- videos/
|   |   |-- images/
|   |   |-- doc/
|   |-- interna-a/
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|     
|-- servicios/
|   |-- evento-a
|   |    |-- videos/
|   |    |-- images/
|   |    |-- doc/
|   |
|   |-- evento-b
|       |-- videos/
|       |-- images/
|       |-- doc/
|   
|   
|
|-- OG/
    |-- img-para-metadata.jpg

````


Para otros landings

````text
landings/
|
|---
|   |-- landing-a/
|   |   |-- videos/
|   |   |-- images/
|   |   |-- doc/
|   |
|   |-- landing-b/
|       |-- videos/
|       |-- images/
|       |-- doc/
|  
|
|-- OG/
    |-- img-para-metadata.jpg

````

Para Opens Portals con CMS's

Debido a que manejan estructuras diferentes en cada caso y no es posible alterar la estructura de ubicación de elementos para seguir el lineamiento estándar de UPC.


