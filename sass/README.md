# SASS

### Estructura de archivos
````text
sass/
|
|-- base/
|   |-- _variables.scss
|   |-- _utility.scss
|   |-- _colors.scss
|   |-- _typography.scss
|   ...
|
|-- layout/
|   |-- _footer.scss
|   |-- _header.scss
|   |-- _sidebar.scss
|   ...
|
|-- components/
|   |-- _login.scss
|   |-- _user.scss
|   ...
|
|-- vendor/
|   |-- _bootstrap.scss
|   ...
|
`-- main.scss
````
En la carpeta **base** colocamos todos nuestros estilos de elementos generales.

En la carpeta **layout** colocamos nuestros estilos referidos a sectores especiales de nuestra aplicación, como son el header, el footer, el nav, etc.

En la carpeta **components** colocamos todos los modulos que se repiten a lo largo de la aplicación. Es importante reconocer aquellos módulos que se repiten para poder abstraerlos.

En el caso de proyectos viejos con grandes archivos CSS, es recomendable intentar reordenar los estilos en archivos y si esto no es posible generar un índice al principio que nos indique que estilos podemos encontrar en el archivo.

### Compilar SASS
Concatenación CSS
```bash
sass --watch sass/main.scss css/main.css
```

Minificado CSS
```bash
sass --watch sass/main.scss css/main.css --style compressed
```
