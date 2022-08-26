# **Tipos de elementos**

En HTML estándar los elementos se clasifican en: **elementos en linea** y en **elementos en bloque**

## **Elementos en bloque**

Siempre empiezan en una nueva línea y ocupan todo el espacio disponible hasta el final de la línea.

ejemplos: `<div>`, `<h1> - <h6>`, `<p>`, `<form>`, `<header>`, `<footer>`, `<section>`, `<ul>`...

## **Elementos en línea**

No empiezan _necesariamente_ en una nueva línea y sólo ocupan el espacio necesario.

ejemplos: `<span>`, `<a>`, `<img>`, `<input>`, `<label>`...

# **Position**

Selecciona el posicionamiento con el que se mostrará el elemento.

OJO!: sólo indica cómo se posiciona una caja, pero no la desplaza.

```css
/* Valores de esta propiedad */
position: static | relative | absolute | fixed;
```

1. ```css
   position: static;
   ```

   Es el posicionamento normal, el elemento estará en el flujo normal de la página.
   **_Se ignoran_** los valores de las propiedades `top`, `right`, `bottom`, `left`.

2. ```css
   position: relative;
   ```

   Con la diferencia de `static` que el desplazamiento de la caja **_se controla_** con las propiedades `top`, `right`, `bottom`, `left`.

   El desplazamiento relativo de una caja no afecta al resto de cajas adyacentes, que se muestran en la misma posición que si la caja desplazada no se hubiera movido de su posición original.

3. ```css
   position: absolute;
   ```

   El desplazamiento de la caja **_se controla_** con las propiedades `top`, `right`, `bottom`, `left`. La posición de una caja se establece de forma absoluta respecto de su elemento contenedor y el resto de elementos de la página se ven afectados y modifican su posición.

   Si se quiere posicionar un elemento de forma absoluta respecto de su elemento contenedor, sólo es necesario añadir la propiedad `position: relative`.

4. ```css
   position: fixed;
   ```
   Es desplazamiento se establece de la **misma forma** que en el posicionamiento `absolute`, pero en este caso el elemento permananece **inmovil** en la pantalla.

# **top, right, bottom, left**

Cuando se posiciona una caja también es necesario **desplazarla** respecto de su **posición original** o respecto de otro origen de coordenadas. Para ello, utilizaremos las propiedades `top`, `right`, `bottom`, `left`.

```css
/* Valores de estas propiedades */
top, right, bottom, left: unidad de medida | porcentaje, auto;
```

De esta forma podemos indicar el **dezplazamiento horizontal o vertical** del elemento respecto de su posición original.

# **Float**

Cuando en una caja usamos el posicionamiento flotante, se convierte en una **_caja flotante_**, lo que significa que se dezplaza o posiciona lo más hacia la izquierda o derecha de la posición original.

DATO: La caja deja de pertenecer al flujo normal de la página, lo que significa que el resto de cajas ocupan el lugar dejado por la caja flotante.

```css
/* Valores del float */
float: left | right | none;
```

1. ```css
   float: left;
   ```

   La caja se **desplaza** hasta el punto más a la **izquierda** posible, el resto de **elementos adyacentes** se adaptan y **fluyen alrededor** de la caja flotante.

2. ```css
   float: right;
   ```

   similar a `float: left` pero la caja se **desplaza** hasta el punto más a la **derecha** posible.

3. ```css
   float: none;
   ```
   **anula** el **posicionamiento flotante** de forma que el elemento se **muestra** en su **posición original**.

## **clear**

La propiedad `clear` modifica el comportamiento por defecto del **posicionamiento flotante**

```css
/* Valores de clear */
clear: none | left | right | both;
```

De esta forma indicamos el **lado del elemento** que **no debe ser adyacente** a ninguna caja flotante.

1. ```css
   clear: left;
   ```

   el **elemento se desplaza** de forma **descendente** hasta que pueda colocarse en una **línea** en la que **no haya** ninguna **caja flotante** en el **lado izquierdo**.

2. ```css
   clear: right;
   ```

   similar a `clear: left` pero en este caso tienen en cuenta los elementos desplazados hacia la derecha

3. ```css
   clear: both;
   ```
   **despeja los lados izquierdo y derecho** del elemento, ya que **desplaza el elemento de forma descendente** hasta que el borde superior se encuentre por debajo del borde inferior de cualquier elemento flotante hacia la izquierda o hacia la derecha.

# **display**

```css
display: inline | block | inline-block;
```

La **propiedad display** permite **ocultar** completamente un **elemento** haciendo que desaparezca de la página. Como el elemento oculto no se muestra, el resto de **elementos** de la página se mueven para **ocupar su lugar**.

1. ```css
   display: block;
   ```

   muestra un **elemento** como si fuera un **elemento de bloque**, independientemente del tipo de elemento que se trate. **Admite** las propiedades `width` y `height`

2. ```css
   display: inline;
   ```

   visualiza un **elemento** en forma de **elemento en línea**, independientemente del tipo de elemento que se trate. **No admite** las propiedades `width` y `height`, además el padding y margin empujan los elementos en horizontal.

3. ```css
   display: inline-block;
   ```

   no agrega un salto de línea después del elemento, por lo que el elemento puede ubicarse junto a otros elementos. **Admite** las propiedades `width` y `height` en el elemento y respetan los márgenes/rellenos superior e inferior.

4. ```css
   display: none;
   ```
   **oculta un elemento** y hace que **desaparezca** de la **página**. El resto de elementos de la página se visualizan como si no existiera el elemento oculto, es decir, pueden **ocupar** el **espacio** en el que se debería visualizar el **elemento**.

# **z-index**

Permite controlar la posición tridimensional de las cajas posicionadas. De esta forma, es posible indicar las cajas que se muestran delante o detrás de otras cajas cuando se producen solapaientos.

DATO: con esta propiedad es posible crear páginas complejas con varios niveles o capas.

```css
/* valores z-index */
z-index: auto | numero;
```

En general la **propiedad** más **común** es un **número entero**, **también** permite el uso de **numeros negativos**, siendo el número 0 como el nivel más bajo por lo general.

OJO: `z-index` **sólo** tiene **efecto** en los **elementos posicionados**, por lo que es obligatorio que `z-index` vaya acompañada de `position`.