# SASS

### Estructura de archivos
````text
styles/
|
|-- base/
|   |-- _utility.scss
|   |-- _colors.scss
|   |-- _typography.scss
|   |-- _buttons.scss
|   ...
|
|-- layout/
|   |-- header.scss
|   |-- footer.scss
|   |-- nav.scss
|   ...
|
|-- components/
|   |-- _user.scss
|   |-- _login.scss
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

### BEM
BEM es una de las tantas convenciones que existen para nombrar a nuestras clases CSS.
Si utilizamos BEM correctamente nuestro CSS sera más claro y semantico.
```css
// CSS

// Bloque
.user-avatar{
    display: inline-block;
    border: 2px solid black;
}

// Elemento
.user-avatar__image{
    border-radius: 5px;
    margin-right: 10px;
}

.user-avatar__label{
    color: green;
    text-transform: uppercase;
}

// Modificador
.user-avatar--big{
    border: 5px solid black;
}


// HTML
div.user-avatar.user-avatar--big
    img.user-avatar__image
    span.user-avatar__label
```

