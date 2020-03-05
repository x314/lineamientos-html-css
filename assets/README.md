# Imágenes e Videos

Para las imágenes, videos y documentos usaremos la plataforma de [cloudinary](https://cloudinary.com/) 
como cnd y optimización de imágenes.

![Alt text](../assets/img/view-cloudinary.png?raw=true "Title")

Para un mejor lineamiento los nombres de las imágenes, video y documentos(pdfs) deben estar:

- En minúsculas.
- Sin tildes.
- Separado en guión si el nombre lo requiere.


#### Estructura 

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



