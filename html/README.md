# HTML

### Plantilla básica
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=Edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no, viewport-fit=cover">

  <title>Título de página menor a 60 caracteres</title>
  <meta name="description" content="Descripción de la página menor a 155 caracteres">
  <meta name="keywords" content="palabra clave 1, palabra clave 2 ...">
  <meta name="author" content="@UPCedu">

  <link rel="icon" type="image/png" href="https://example.com/favicon.png">

  <link rel="stylesheet" href="css/main.css">

  <!-- Facebook Open Graph -->

  <!-- Twitter Card -->

  <!-- Google Tag Manager -->
  <script>
    (function (w, d, s, l, i) {
      w[l] = w[l] || [];
      w[l].push({
        'gtm.start': new Date().getTime(),
        event: 'gtm.js'
      });
      var f = d.getElementsByTagName(s)[0],
        j = d.createElement(s),
        dl = l != 'dataLayer' ? '&l=' + l : '';
      j.async = true;
      j.src =
        'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
      f.parentNode.insertBefore(j, f);
    })(window, document, 'script', 'dataLayer', 'GTM-XXXXXXX');
  </script>
  <!-- End Google Tag Manager -->
</head>
<body>

<!-- Google Tag Manager (noscript) -->
  <noscript>
    <iframe src="https://www.googletagmanager.com/ns.html?id=GTM-XXXXXXX" height="0" width="0"
      style="display:none;visibility:hidden"></iframe>
  </noscript>
  <!-- End Google Tag Manager (noscript) -->

  <header></header>
  <section></section>
  <footer></footer>

  <script src="example.js"></script>

</body>
</html>
```

**Doctype:** El doctype es HTML5 y se localiza arriba del todo en tus páginas HTML
```html
<!DOCTYPE html>
```

**Atributo de idioma:** Indicamos el idioma definido para la página actual
```html
<html lang="es">
```

**Codificación de caracteres:** Declaramos la codificación de juego de caracteres para el documento
```html
<meta charset="UTF-8">
```

**Modo de compatibilidad IE:** Ordenamos a Internet Explorer usar su motor de renderizado más reciente
```html
<meta http-equiv="X-UA-Compatible" content="IE=Edge">
```

**Viewport:** Para diseño web responsivo
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0, shrink-to-fit=no, viewport-fit=cover">
```

**Título:** El límite en los títulos es no mayor a 60 caracteres. En ellos se indicará el contenido de la página y el dominio de su portal.
> **Nota:** Si la definición de la página no puede acortarse a los cantidad indicada, los que se encuentren luego de los 60 caracteres deberán ser considerados dentro de la descripción.
```html
<title>Malla curricular | Comunicación y Periodismo | Pregrado UPC</title>
```

**Descripción:** Una meta descripción es proporcionada, es única y no es mayor a 155 caracteres. En ellos se definirá el contenido de la página incluyendo el nombre.
```html
<meta name="description" content="Conoce la malla curricular de la carrera Comunicación y Periodismo de la UPC. Descubre una enseñanza integral que desarrolla tus habilidades.">
```

**Palabras clave:** Se deberá incluir entre 5 y 8 palabras clave, separadas por comas, relacionadas al contenido de la misma.
> **Nota:** dentro de las palabras clave no se consideran tildes.
```html
<meta name="keywords" content="Malla curricular comunicacion y periodismo, curricula periodismo upc, malla curricular periodismo, cursos comunicacion y periodismo, comunicacion y periodismo upc, cursos de periodismo, cursos de carrera periodismo">
```

**Autor:** Propietario de los derechos del código fuente de una página HTML
```html
<meta name="author" content="@UPCedu">
```

**Favicons:** Si solo tienes un `favicon.ico`, colocalo en la raíz de tu sitio. Normalmente no necesitarás usar ningún marcado. Sin embargo, es una buena práctica enlazarlo usando el ejemplo debajo. Actualmente, **se recomienda el formato PNG** sobre el formato `.ico` (dimensión: 32x32px).
```html
<!-- Favicon estandar -->
<link rel="icon" type="image/x-icon" href="https://example.com/favicon.ico">
<!-- Formato favicon recomendado -->
<link rel="icon" type="image/png" href="https://example.com/favicon.png">
```

**Incluir CSS y JavaScript:** Según la especificación de HTML5, no es necesario especificar un tipo cuando se incluyen archivos CSS y JavaScript, ya que `text/css` y `text/javascript` son valores predeterminados.
> **Nota:** Todos los archivos CSS son cargados antes que cualquier archivo JavaScript (Excepto en los casos donde los archivos JS se cargan asíncronamente)
```html
<!-- CSS -->
<link rel="stylesheet" href="example.css">

<!-- JavaScript -->
<script src="example.js"></script>
```

**Facebook Open Graph:** Las imágenes necesitan ser de al menos 600 x 315 pixeles, se recomienda 1200 x 630 pixeles.
> **Nota:** Al usar og:image:width y og:image:height se especificaran las dimensiones de la imagen al crawler para que pueda desplegar la imagen inmediatamente sin tener que descargarla y procesarla asíncronamente.
```html
<meta property="og:type" content="website">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:title" content="Título del contenido">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:description" content="Descripción aquí">
<meta property="og:site_name" content="Nombre del sitio">
<meta property="og:locale" content="es_ES">
<!-- Las siguientes etiquetas son opcionales, pero recomendadas -->
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```
> [Depurador de contenido compartido](https://developers.facebook.com/tools/debug/)

**Twitter Card:**
```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@UPCedu">
<meta name="twitter:creator" content="@UPCedu">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Título del contenido">
<meta name="twitter:description" content="Descripción del contenido menor a 200 caracteres">
<meta name="twitter:image" content="https://example.com/image.jpg">
```
> [Twitter card validator](https://cards-dev.twitter.com/validator)

**Google Tag Manager:**  
Antes del cierre de la etiqueta `</head>`
```html
<!-- Google Tag Manager -->
<script>
  (function (w, d, s, l, i) {
    w[l] = w[l] || [];
    w[l].push({
      'gtm.start': new Date().getTime(),
      event: 'gtm.js'
    });
    var f = d.getElementsByTagName(s)[0],
      j = d.createElement(s),
      dl = l != 'dataLayer' ? '&l=' + l : '';
    j.async = true;
    j.src =
      'https://www.googletagmanager.com/gtm.js?id=' + i + dl;
    f.parentNode.insertBefore(j, f);
  })(window, document, 'script', 'dataLayer', 'GTM-XXXXXXX');
</script>
<!-- End Google Tag Manager -->
```

Justo después de abrir la etiqueta `<body>`
```html
<!-- Google Tag Manager (noscript) -->
  <noscript>
    <iframe src="https://www.googletagmanager.com/ns.html?id=GTM-XXXXXXX" height="0" width="0"
      style="display:none;visibility:hidden"></iframe>
  </noscript>
  <!-- End Google Tag Manager (noscript) -->
```

### Reglas generales
**Usar tabulaciones con dos espacios:** son la única forma de garantizar que el código se reproduzca de la misma manera en cualquier entorno.  
**Siempre usar comillas dobles:** nunca comillas simples, en los atributos.  
**No incluya una barra inclinada** en los elementos de cierre automático (por ejemplo, `<img>`).  
**Noopener:** En caso que uses enlaces externos con `target="_blank"`, tu enlace debe tener un atributo `rel="noopener"` para evitar tab nabbing. Si necesitas dar soporte a versiones antigüas de Firefox, usa `rel="noopener noreferrer"`.  
**Limpiar comentarios:** Código innecesario necesita ser removido antes de enviar la página a producción.  
**Orden de atributos:** Los atributos HTML deben venir en este orden para facilitar la lectura del código.
- `class`
- `id`, `name`
- `data-*`
- `src`, `for`, `type`, `href`, `value`
- `title`, `alt`
- `role`, `aria-*`
```html
<a class="..." id="..." data-toggle="modal" href="#">
  Example link
</a>

<input class="form-control" type="text">

<img src="..." alt="...">
```
**Atributos booleanos:** Es aquel que no necesita un valor declarado. XHTML requería que declararas un valor, pero HTML5 no tiene tal requisito.
```html
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
  <option value="1" selected>1</option>
</select>
```

### Pruebas HTML - [W3C developers](https://www.w3.org/developers/tools/)
**W3C:** Todas las páginas necesitan ser aprobadas por el validador W3C para identificar posibles problemas en el código HTML.
> [W3C validator](https://validator.w3.org/)

**PageSpeed Insights:** Mejora la velocidad de tus páginas web en todos los dispositivos.
> [Analizar](https://developers.google.com/speed/pagespeed/insights/)

**Prueba de optimización para móviles:** Comprueba si un visitante puede usar fácilmente tu página en un dispositivo móvil. 
> [Probar URL](https://search.google.com/test/mobile-friendly)

**Verificador de enlaces:** No hay enlaces rotos en la página, verifica que no tienes ningún error 404.
> [W3C Link Checker](https://validator.w3.org/checklink)
