# CSS

### BEM
BEM es una convención de nomenclatura para nuestras clases CSS.
Si utilizamos BEM correctamente nuestro CSS sera más claro y semántico.
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

### Reglas generales
- Usar tabulaciones con dos espacios, son la única forma de garantizar que el código se reproduzca de la misma manera en cualquier entorno.
- Al agrupar los selectores, mantenga los selectores individuales en una sola línea.
- Incluya un espacio antes de la apertura de los bloques de declaración para legibilidad.
- Cada declaración debe aparecer en su propia línea para un informe de errores más preciso.
- Todos los valores hexadecimales en minúsculas, por ejemplo, `#fff`. Las letras minúsculas son mucho más fáciles de discernir cuando se escanea un documento, ya que tienden a tener formas más únicas.
- Use valores abreviados hexadecimales donde esté disponible, por ejemplo, `#fff` en lugar de `#ffffff`.
- Indique los valores de los atributos en los selectores, por ejemplo, ingrese `[type="text"]`. Solo son opcionales en algunos casos, y es una buena práctica para la consistencia.
- Evite especificar unidades para valores cero, por ejemplo, `margin: 0;` en lugar de `margin: 0px;`.
```css
/* Mal */
.selector, .selector-secondary, .selector[type=text] {
  padding:15px;
  margin:0px 0px 15px;
  background-color:rgba(0, 0, 0, 0.5);
  box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF
}

/* Bien */
.selector,
.selector-secondary,
.selector[type="text"] {
  padding: 15px;
  margin-bottom: 15px;
  background-color: rgba(0,0,0,.5);
  box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #fff;
}
```

### Orden de declaración
Las declaraciones de propiedades relacionadas se deben agrupar siguiendo el orden:

1. Posicionamiento
2. Modelo de caja
3. Tipográfico
4. Visual

> El posicionamiento es lo primero porque puede eliminar un elemento del flujo normal del documento y anular los estilos relacionados con el modelo de cuadro. El modelo de caja viene a continuación, ya que dicta las dimensiones y la ubicación de un componente.  
Todo lo demás tiene lugar dentro del componente o sin afectar a las dos secciones anteriores, y por lo tanto, son las últimas.

```css
.selector {
  /* Posicionamiento */
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: 100;

  /* Modelo de caja */
  display: block;
  float: right;
  width: 100px;
  height: 100px;

  /* Tipográfico*/
  font: normal 13px "Helvetica Neue", sans-serif;
  line-height: 1.5;
  color: #333;
  text-align: center;

  /* Visual */
  background-color: #f5f5f5;
  border: 1px solid #e5e5e5;
  border-radius: 3px;

  /* Misc */
  opacity: 1;
}
```

### No usar `@import`
Comparado con `<link>`, `@import` es más lento, agrega solicitudes de página adicionales y puede causar otros problemas imprevistos.
```html
<!-- Usar elementos de enlace -->
<link rel="stylesheet" href="example.css">

<!-- Evitar @imports -->
<style>
  @import url("example.css");
</style>
```

### Declaraciones únicas
El factor clave aquí es la detección de errores, por ejemplo, un validador de CSS que indica que tiene un error de sintaxis en la línea 183. Con una sola declaración, no hay problema. Con múltiples declaraciones, las líneas separadas son una necesidad para su entendimiento.

```css
/* Declaraciones únicas en una línea */
.span1 { width: 60px; }
.span2 { width: 140px; }
.span3 { width: 220px; }

/* Múltiples declaraciones, una por línea. */
.sprite {
  display: inline-block;
  width: 16px;
  height: 15px;
  background-image: url(../img/sprite.png);
}
.icon           { background-position: 0 0; }
.icon-home      { background-position: 0 -20px; }
.icon-account   { background-position: 0 -40px; }
```

### Notación abreviada
Trate de limitar el uso de declaraciones abreviadas a instancias en las que debe establecer explícitamente todos los valores disponibles. Las propiedades comunes de uso abreviado incluyen:
- `padding`
- `margin`
- `font`
- `background`
- `border`
- `border-radius`
```css
/* Mal */
.element {
  margin: 0 0 10px;
  background: red;
  background: url("image.jpg");
  border-radius: 3px 3px 0 0;
}

/* Bien */
.element {
  margin-bottom: 10px;
  background-color: red;
  background-image: url("image.jpg");
  border-top-left-radius: 3px;
  border-top-right-radius: 3px;
}
```
> [Propiedades abreviadas](https://developer.mozilla.org/es/docs/Web/CSS/Shorthand_properties)

### Nombres de clase
- Mantenga las clases en minúsculas y utilice guiones (no guiones bajos o camelCase). Los guiones sirven como saltos naturales en la clase relacionada (por ejemplo, `.btn` y `.btn-danger`).
- Evitar la notación taquigráfica excesiva y arbitraria. `.btn` es útil para el botón, pero `.s` no significa nada.
- Mantenga las clases lo más cortas y concisas posible.
- Clases de prefijo basadas en la clase primaria o base más cercana.
- Use clases `.js-*` para denotar el comportamiento (a diferencia del estilo), pero mantenga estas clases fuera de su CSS.
```css
/* Mal */
.t { ... }
.red { ... }
.header { ... }

/* Bien */
.tweet { ... }
.important { ... }
.tweet-header { ... }
```

### Organización
- Organizar secciones de código por componente.
- Desarrollar una jerarquía de comentarios consistente.
- Cuando utilice varios archivos CSS, divídalos por componente en lugar de página. Se pueden reorganizar las páginas y mover los componentes.
```css
/*
 * Título de la sección de componente
 */
.element { ... }


/*
 * Título de la sección de componente
 *
 * A veces es necesario incluir un contexto opcional para todo el componente. 
Haz eso aquí si es lo sumamente importante.
 */
.element { ... }

/* Subcomponente o modificador */
.element-heading { ... }
.element--modifier { ... }
```


### Pruebas CSS
**W3C:** Todas las páginas necesitan ser aprobadas por el validador W3C para identificar posibles problemas en el código HTML.
> [W3C validator](https://jigsaw.w3.org/css-validator/)

Todas las páginas fueron probadas en todos los navegadores actuales (Chrome, Firefox, Edge, Safari...), navegadores móviles actuales (Navegador nativo, Chrome, Safari...) y Sistemas Operativos actuales (Windows, Mac, Android, iOS).
