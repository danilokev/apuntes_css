# Selectores
## **Selector de tipo o etiqueta (elemento)**
Selecciona elementos html (h1, h2, p, img, body...)
```css
h1 {
  color: red;
}

h2 {
  color: blue;
}

p {
  color: black;
}
```
Se pueden agrupar los elementos y darles un mismo estilo a todas. (***selector múltiple***)
```css
h1, h2, h3 {
  color: #8A8E27;
  font-weight: normal;
  font-family: Arial, Helvetica, sans-serif;
}
```
## **Selector universal**
Selecciona ***todos*** los elementos de la página. Se indica mediante el simbolo *.
```css
* {
  margin: 0;
  padding: 0;
}
```
## **Selector descendente**
Selecciona los elementos que se encuentran dentro de otros elementos. Es decir, cuando se encuentra entre las etiquetas de apertura y de cierre del otro elemento. (El último selector escrito es al que se aplica los estilos)

Sintaxis:
```
selector1 selector2 selector3 ... selectorN
```

Por ejemplo, El selector del siguiente ejemplo selecciona todos los elementos `<span>` de la página que se encuentren dentro de un elemento `<p>`: 
```css
p span { color: red; }
```
Otro ejemplo más complejo:
```css
p a span em { text-decoration: underline; }
```
Los estilos de la regla anterior se aplican a los elementos de tipo `<em>` que se encuentren dentro de elementos de tipo `<span>`, que a su vez se encuentren dentro de elementos de tipo `<a>` que se encuentren dentro de elementos de tipo `<p>`.
## **Selector de clase**
Selecciona los elementos html con un atributo de clase.

Sintaxis:
```css
.nombreclase { propiedades de estilo }
```
Se puede leer como: *"cualquier elemento de la página cuyo atributo class sea igual a nombreclase"*

También podemos seleccionar elementos html para que se vean afectados por una clase:
```css
p.center { 
  text-aling: center;
  color: red 
}
```
Con la expresión anterior ***todos*** los elementos `<p>` con la class="center" tendrán estilos.

Otro ejemplo:
```css
p .center { ... }
```
Con esta expresión seleccionamos los elementos con la class="center" que esten dentro del elemento `<p>`.

Se pueden escribir varias clases sobre un mismo elemento.
```html
<p class="especial destacado error"> Párrafo de texto...</p>
```
## **Selectores de ID**
Selecciona un **único** elemento de la página. (no se puede repetir en dos elementos diferentes de una misma página.)

Sintaxis:
```css
#id_value { propiedades de estilo }
```
Ejemplo:
```css
#center {
  text-aling: center;
  color: red 
}
```
Con esta expresión el elemento con el id="center" tendrá estilos.

El siguiente ejemplo aplica la regla CSS solamente al elemento de tipo `<p>` que tenga un atributo id igual al indicado:
```css
p#center {
  text-aling: center;
  color: red;
}
```

