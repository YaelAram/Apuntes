## Calcular el Tamaño de una Caja

Para calcular el ancho debemos realizar la siguiente suma:

$$
Ancho = BorderIzqDer + PaddingIzqDer + AnchoContenido
$$

Para calcular el alto debemos realizar la siguiente suma:

$$
Alto = BorderArrAba + PaddingArrAba + AltoContenido
$$
## Propiedad Box-Sizing

Como se puede observar, propiedades como *padding* o *border* pueden variar el tamaño y requerimos realizar un par de cálculos para que el tamaño final de la caja sea el que nosotros deseamos pero existe una propiedad en CSS llamada *box-sizing* que nos evita tener que realizar ese par de cálculos e indicar de una forma sencilla el tamaño final que deseamos para el contenedor.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)

La propiedad *box-sizing* le indica a CSS como debe de calcular las dimensiones de un elemento, este puede tomar dos valores:

- **Content-box**: Es el comportamiento por defecto, las propiedades *width* o *height* modifican solo el tamaño del *contenido*, por lo que los anchos *padding* y *border* son agregados al renderizado final, haciendo al elemento más ancho.

```
/* Ancho Final: 5 + 5 + 100 + 5 + 5 = 120px */
/* Ancho Final: 5 + 5 + 50 + 5 + 5 = 70px */
width: 100px;
height: 50px;
border: 5px;
padding: 5px;
```

- **Border-box**: Este comportamiento le indica al navegador que debe considerar *border* y *padding* dentro del calculo del ancho y alto del elemento, por lo que el *contenido* se encoge para compensar el espacio extra generado por el *border* y *padding*.

```
/* Ancho Final: 100px (Ancho Contenido: 80px) */
/* Ancho Final: 50px (Alto Contenido: 30px) */
box-sizing: border-box;
width: 100px;
height: 50px;
border: 5px;
padding: 5px;
```