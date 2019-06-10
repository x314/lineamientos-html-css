# SASS

### Estructura de archivos
````text
sass/
|
|-- base/
|   |-- _mixins.scss
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
|   |-- _profile.scss
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

Los únicos archivos a modificar son los que se encuentran dentro de las carpetas, el archivo `main.scss` solo debe importar lo desarrollado.

En el caso de proyectos viejos con grandes archivos CSS, es recomendable intentar reordenar los estilos en archivos y si esto no es posible generar un índice al principio que nos indique que estilos podemos encontrar en el archivo.

### Compilar SASS
Concatenación CSS
```bash
sass --watch sass/main.scss:css/main.css
```

Minificado CSS
```bash
sass --watch sass/main.scss:css/main.css --style compressed
```

### .map
Los archivos `.map` buscan cerrar la brecha entre los lenguajes de nivel superior como Sass y los lenguajes de nivel inferior que compilan (CSS). Permiten ver la fuente original (Sass) en lugar del CSS compilado mientras se realiza la depuración.

En la práctica, para los usuarios de Sass, esto significa que cuando inspecciona un elemento con herramientas de desarrollador, en lugar de ver los estilos CSS asociados con ese elemento, puede ver el código que realmente nos importa: el Sass precompilado.
