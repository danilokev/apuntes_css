# **MODEL DE CAJA**

![box-model](https://s3-us-west-2.amazonaws.com/devcodepro/media/tutorials/modelo-caja-css-t1.jpg)

## **width (anchura)**

controla la **anchura** de la caja de los **elementos**.

```css
width: unidades de medida (px, rem...) | % | auto;
```

## **height (altura)**

Controla la **altura** de los elementos.

```css
height: unidades de medida (px, rem...) | % | auto;
```

## **padding (relleno)**

Crea **espacio** alrededor del **contenido** de un **elemento**.

```css
padding: unidades de medida (px, rem...) | %;
```

Tenemos cuatro propiedades del padding para controlar cada lado del elemento.
`padding-top`, `padding-right`, `padding-bottom`, `padding-left`.

Algunas abrevaciones del padding según los valores:

- 4 valores: `padding: 25px 50px 75px 100px;`
  estos valores aplican a _padding-top, padding-right, padding-bottom y padding-left_ respectivamente.

- 3 valores: `padding: 25px 50px 75px;`
  estos valores aplican a _padding-top, padding-right/padding-left y padding-bottom_ respectivamente.

- 2 valores: `padding: 25px 50px;`
  estos valores se aplican a _paddding-top/padding-bottom y padding-right/padding-left_ respectivamente.

## **border (borde)**

Establece el borde de un elemento mediante el **ancho, estilo y color**.

```css
border: border-width border-style border-color;
```

### 1. **border-width**

Establece el **ancho** de todos los **bordes** del **elemento**.

```css
border-width: border-top border-right border-bottom border-left;
```

algunos valores de `borde-width` son: unidades de medida (px, em...) o `thin`, `medium`, `thick`.

- 4 valores: `border-width: 25px 50px 75px 100px;`
  el orden de aplicación es superior, derecho, inferior e izquierdo.

- 3 valores: `border-width: 25px 50px 75px;`
  el primero se aplica al borde superior, el segundo se aplica al borde izquierdo y derecho y el tercer valor se aplica al borde inferior
- 2 valores: `border-width: 25px 50px;`
  el primero se aplica al borde superior e inferior y el segundo valor se aplica al borde izquierdo y derecho

La **anchura de cada uno de los bordes** se controla con las cuatro propiedades siguientes:

```css
border-top-width, border-right-width, border-bottom-width, border-left-width
```

### 2. **border-style**

Establece el **estilo** de cada uno de los cuatro **bordes** del **elemento**.

```css
border-style: border-top border-right border-bottom border-left;
```

algunos valores de `border-style` son: `none`, `hidden`, `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`.

![border-style](https://uniwebsidad.com/static/libros/imagenes/css/f0413.gif)

- 4 valores: `border-style: solid solid solid solid;`
  el orden de aplicación es superior, derecho, inferior e izquierdo.

- 3 valores: `border-style: solid solid solid;`
  el primero se aplica al borde superior, el segundo se aplica al borde izquierdo y derecho y el tercer valor se aplica al borde inferior

- 2 valores: `border-style: solid solid;`
  el primero se aplica al borde superior e inferior y el segundo valor se aplica al borde izquierdo y derecho

CSS permite establecer el **estilo de cada uno de los bordes** mediante las siguientes propiedades:

```css
border-top-style, border-right-style, border-bottom-style, border-left-style
```

### 3. **border-color**

Establece el **color** de los **bordes** del **elemento**.

```css
border-color: border-top border-right border-bottom border-left;
```

algunos valores de `border-color` son:
`transparent, currentcolor, rgb(255, 0, 0), rgba(255, 0, 0, 0.5), #ff0000, red, blue, green, black, white, gray, silver, yellow, orange, pink, purple, brown, maroon, lime, aqua, fuchsia, olive, teal`.

- 4 valores: `border-color: rgb(255, 0, 0) rgb(0, 255, 0) rgb(0, 0, 255) rgb(255, 255, 255);`
  el orden de aplicación es superior, derecho, inferior e izquierdo.

- 3 valores: `border-color: rgb(255, 0, 0) rgb(0, 255, 0) rgb(0, 0, 255);`
  el primero se aplica al borde superior, el segundo se aplica al borde izquierdo y derecho y el tercer valor se aplica al borde inferior

- 2 valores: `border-color: rgb(255, 0, 0) rgb(0, 255, 0);`
  el primero se aplica al borde superior e inferior y el segundo valor se aplica al borde izquierdo y derecho

Para controlar el **color de cada uno de los bordes** se utiliza las siguientes propiedades:

```css
border-top-color, border-right-color, border-bottom-color, border-left-color
```

## **margin (margen)**

Crea espacio **alrededor** del **contenido** de un **elemento**, fuera de los bordes.

```css
margin: margin-top margin-right margin-bottom margin-left;
```

algunos valores de `margin` son: unidades de medida (px, em...) | % | auto.

- 4 valores: `margin: 25px 50px 75px 100px;`
  el orden de aplicación es superior, derecho, inferior e izquierdo.

- 3 valores: `margin: 25px 50px 75px;`
  el primero se aplica al margen superior, el segundo se aplica al margen izquierdo y derecho y el tercer valor se aplica al margen inferior

- 2 valores: `margin: 25px 50px;`
  el primero se aplica al margen superior e inferior y el segundo valor se aplica al margen izquierdo y derecho

## **backgrounds (fondos)**

### 1. **background-color**

Establece el **color** del **fondo** del **elemento**.

```css
background-color: red;
```

algunos valores de `background-color` son: `transparent`, `currentcolor`, `rgb(255, 0, 0)`, `rgba(255, 0, 0, 0.5)`, `#ff0000`, `red`, `blue`, `green`, `black`, `white`, `gray`, `silver`, `yellow`, `orange`, `pink`, `purple`, `brown`, `maroon`, `lime`, `aqua`, `fuchsia`, `olive`, `teal`.

## 2. **background-image**

permite mostrar una imagen como fondo de la caja de cualquier elemento:

```css
background-image: url('imagen.png');
```

Podemos crear una carpeta con imágenes y añadirlas a la carpeta **images** del proyecto.

## 3. **background-repeat**

Para que la imagen de fondo se repita horizontal y verticalmente

```css
background-repeat: repeat-x;
```

- Horizontalmente: `background-repeat: repeat-x;`

- Verticalmente: `background-repeat: repeat-y;`

- no repite: `background-repeat: no-repeat;`

## 4. **background-position**

Para controlar la posición de la imagen dentro del fondo del elemento.

```css
background-position: center;
```

- centro: `background-position: center;`

- arriba: `background-position: top;`

- abajo: `background-position: bottom;`

- izquierda: `background-position: left;`

- derecha: `background-position: right;`

- porcentajes: `background-position: 50% 50%;`

podemos combinar estos valores: `left top`, `left center`, `left bottom`, `right bottom`, `right top`...

## 5. **background-attachment**

Para que el fondo permanezca fijo cuando la ventana del navegador se desplaza mediante las barras de scroll.

```css
background-attachment: fixed;
```

algunos valores de `background-attachment` son: `scroll`, `fixed`, `local`.

## 6. **background**

propiedad de tipo "shorthand" para indicar todas las propiedades de los colores e imágenes de fondo de forma directa. La propiedad se denomina `background` y es la que generalmente se utiliza para establecer las propiedades del fondo de los elementos.

```css
background: background-color background-image background-repeat
  background-attachment background-position;
```

El orden en el que se indican las propiedades es indiferente, aunque en general se sigue el formato indicado de color, url de imagen, repetición y posición..

Ejemplo:

```css
/* Color e imagen de fondo de la página mediante una propiedad shorthand */
body {
  background: #222d2d url(./graphics/colorstrip.gif) repeat-x 0 0;
}

/* La propiedad shorthand anterior es equivalente a las siguientes propiedades */
body {
  background-color: #222d2d;
  background-image: url('./graphics/colorstrip.gif');
  background-repeat: repeat-x;
  background-position: 0 0;
}
```
