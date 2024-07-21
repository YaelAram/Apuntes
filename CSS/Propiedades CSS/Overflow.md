El *overflow* sucede cuando tenemos un elemento HTML de tamaño fijo cuyo contenido ya sea por su tamaño o cantidad no es capaz de envolver provocando que se desborde (usualmente mostrando el contenido aun cuando este fuere de los limites del elemento).

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow)

**Nota: Esta propiedad es un atajo a las propiedades *overflow-x* y *overflow-y*.**

La propiedad CSS *overflow* nos permite indicarle al navegador como deseamos que se ajuste el contenido cuando este se desborde tanto en el eje vertical como horizontal:

- **Visible**: Este es el valor por defecto. El contenido desbordado sigue siendo mostrado a pesar de que este este fuera de los limites del elemento, el elemento no adquiere barras de desplazamiento en ninguno de sus ejes.
- **Hidden**: Este valor oculta todo el contenido que desborde los limites del elemento HTML, el contenido es cortado siguiendo los bordes del elemento por lo que no hay control del como este es cortado (ocultado). El elemento no adquiere barras de desplazamiento en ninguno de sus ejes.

```
overflow: hidden;
```

- **Scroll**: Este valor tiene un comportamiento similar a *hidden*, oculta todo lo que este más allá del borde con la diferencia que este habilita las barras de desplazamiento en ambos ejes (eje X y Y) lo que nos permite visualizar el contenido que fue ocultado para evitar el desborde.

**Nota: Debido a que la propiedad *overflow* es un atajo de las propiedad *overflow-x* y *overflow-y* las barras de desplazamiento serán mostradas en ambos ejes a pesar de solo requerir uno de ellos.**

```
overflow: scroll;
```

- **Clip**: Es valor es un punto medio entre los valores *hidden* y *visible* ya que nos permite definir un espacio en el cual el desbordamiento es mostrado a pesar de estar fuera de los limites del elemento (*visible*) pero una vez sobrepasado ese limite el contenido desbordado es ocultado (*hidden*). Este tipo de desbordamiento debe ser acompañado por una propiedad llamada *overflow-clip-margin* la cual le indica el espacio en el cual el contenido desbordado debe ser visible.

```
overflow: clip;
overflow-clip-margin: 20px
```

- **Auto**: Nos permite dejar la decisión en el navegador, si el contenido cabe en el contenedor este actúa como el valor *visible* si el contenido se desborda el navegador muestra las barras de desplazamiento necesarias (a diferencia de *scroll* solo muestra las barras de desplazamiento necesarias para que el usuario pueda ver el contenido oculto).

```
overflow: auto;
```