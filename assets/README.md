# Lineamientos  imágenes,videos y documentos

Para las imágenes, videos y documentos usaremos la plataforma de [cloudinary](https://cloudinary.com/) 
como cdn y optimización de imágenes.

![Alt text](../assets/img/view-cloudinary.png?raw=true "Cloudinary")

Para un mejor lineamiento  las imágenes, video y documentos deben estar:

- En minúsculas.
- Sin tildes.
- Separado en guión(-) si el nombre lo requiere.
- Formatos de videos en mp4 y webm.
- Formatos de imágenes svg,png y jpg.

Nota: NO se aceptan estas formas de nombrar archivos.
  
  - MI_ARCHIVO$.pdf
  - Imagen_de_Presentación.PNG
  - mI_Video@-upc.mp4
  - NUEVO_Video@-upc100%.webm

#### Cloudinary

Al momento de acceder a la plataforma seleccionar la pestaña de "Media Library"
se mostrara los repositorios de las páginas upc inluido los open portals

![Alt text](../assets/img/cloudinary1.png?raw=true "Cloudinary1")


#### Estructura General





#### Estructuras 

Para imágenes globales como logos upc o wasc 
- Los logos upc deben estar en formato svg (rojo y blanco).
- Las imágenes para redes sociales en formato png.

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
|       |-- img/
|       |-- doc/
|   
|
|-- facultades/
|   |-- facultad-a
|   |   |-- videos/
|   |   |-- img/
|   |   |-- doc/
|   |
|   |-- facultad-b
|       |-- videos/
|       |-- img/
|       |-- doc/
|   
|
|-- modalidades/
|   |-- modalidad-a
|   |   |-- videos/
|   |   |-- img/
|   |   |-- doc/
|   |
|   |-- modalidad-b
|       |-- videos/
|       |-- img/
|       |-- doc/
|
|   
|-- eventos/
|   |-- evento-a
|   |    |-- videos/
|   |    |-- img/
|   |    |-- doc/
|   |
|   |-- evento-b
|       |-- videos/
|       |-- img/
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
|   |-- img/
|   |-- doc/
|   
|
|-- carreras/
|   |-- carrera-a/
|       |-- videos/
|       |-- img/
|       |-- doc/
|   
|     
|-- eventos/
|   |-- evento-a
|   |    |-- videos/
|   |    |-- img/
|   |    |-- doc/
|   |
|   |-- evento-b
|       |-- videos/
|       |-- img/
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
|   |-- img/
|   |-- doc/
|   
|
|-- noticias/
|   |-- carrera-a/
|       |-- videos/
|       |-- img/
|       |-- doc/
|
|-- internas/
|   |-- interna-a/
|   |   |-- videos/
|   |   |-- img/
|   |   |-- doc/
|   |-- interna-a/
|       |-- videos/
|       |-- img/
|       |-- doc/
|   
|     
|-- servicios/
|   |-- evento-a
|   |    |-- videos/
|   |    |-- img/
|   |    |-- doc/
|   |
|   |-- evento-b
|       |-- videos/
|       |-- img/
|       |-- doc/
|   
|   
|
|-- OG/
    |-- img-para-metadata.jpg

````

Para Otros Landings

````text
landings/
|
|---
|   |-- landing-a/
|   |   |-- videos/
|   |   |-- img/
|   |   |-- doc/
|   |
|   |-- landing-b/
|       |-- videos/
|       |-- img/
|       |-- doc/
  
|
|-- OG/
    |-- img-para-metadata.jpg

````


