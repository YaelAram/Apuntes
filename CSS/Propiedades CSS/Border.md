Esta propiedad es un atajo a las propiedades *border-width*, *border-style* y *border-color*, nos permite modificar el ancho, estilo y color de todos los bordes de un elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/border)

```
border: 1px solid black;
```
## Border-Width

Esta propiedad es un atajo a las propiedades *border-top-width*, *border-right-width*, *border-bottom-width* y *border-left-width*, nos permite establecer el ancho del borde de un elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)

Esta propiedad admite los siguientes tipos de dato:

- Unidades absolutas.
- Unidades relativas.

```
border-width: 1px; /* Todos los bordes */
border-width: 1px 2px; /* Top/Bottom Left/Right */
border-width: 1px 2px 1px; /* Top Left/Right Bottom */
border-width: 1px 2px 3px 4px; /* Top Right Bottom Left */
```
## Border-Style

Esta propiedad es un atajo para las propiedades *border-top-style*, *border-right-style*, *border-bottom-style* y *border-left-style*. Nos permite indicar un estilo al borde del elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)

Admite los siguientes valores:

- **None**: Este es el valor por defecto. No muestra ningún borde en el elemento a pesar que este tenga un borde definido.
- **Dotted**: Este valor muestra el borde como una serie de puntos separados entre si por un pequeño espacio.
- **Dashed**: Similar al valor *dotted* pero en lugar de puntos muestra lineas.
- **Solid**: Este valor provoca un borde continuo.
- **Double**: Similar al valor *solid* pero muestra dos bordes continuos.

```
border-style: solid; /* Todos los bordes */
border-style: solid dotted; /* Top/Bottom Left/Right */
border-style: solid dotted double; /* Top Left/Right Bottom */
border-style: solid dotted double dashed; /* Top Right Bottom Left */
```
## Border-Color

Esta propiedad es un atajo a las propiedades  *border-top-color*, *border-right-color*, *border-bottom-color* y *border-left-color*. Tambien es un atajo a las propiedades *border-block-start-color*, *border-block-end-color*, *border-inline-start-color* y *border-inline-end-color* que son propiedades que se adaptan al valor de la propiedad *writing-mode*. Nos permite cambiar el color del borde de un elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color)

Esta propiedad acepta cualquier método para especificar color soportado por CSS.

```
border-color: red; /* Todos los bordes */
border-color: blue red; /* Top/Bottom Left/Right */
border-color: blue red cyan; /* Top Left/Right Bottom */
border-color: blue red cyan green; /* Top Right Bottom Left */
```