Esta propiedad determina como un elemento es posicionado dentro del elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/position)
#### Static

Este es el valor por defecto. El elemento es posicionado siguiendo el flujo normal HTML. Las propiedades *top*, *bottom*, *left*, *right* y *z-index* son ignoradas.
#### Absolute

Este valor remueve el elemento del flujo normal del documento HTML por lo que dentro del contenido renderizado no se crea espacio para alojarlo. El elemento puede ser movido de lugar utilizando las propiedades *top*, *bottom*, *right* y *left* o la propiedad *inset*.

```
<section>
	<div>Container</div>
</section>
```

```
div {
	position: absolute;
	top: 0;
	right: 0; /* inset: 0 0 auto auto */
}
```

En este ejemplo, el elemento *div* es posicionado en la esquina superior derecha del viewport, sin ningún margin que lo separe de los bordes.

Si por otro lado requerimos que modificar la posición del elemento sin que este abandone los limites del elemento padre, entonces debemos agregar la siguiente propiedad al elemento padre:

```
section {
	position: relative;
}
```

**Nota: El movimiento realizado por el elemento es realizado respecto al primer elemento padre que contenga un *position: relative*, si no hay ninguno entonces se realiza el movimiento del elemento respecto al *viewport*.**

**Nota: Básicamente esta propiedad nos permite mover un elemento dentro de los limites del primer contenedor padre con el atributo *position: relative* o el *viewport* en su defecto.**

**Nota: Al aplicar esta propiedad el elemento se encuentra en una capa superior, por lo que al moverse puede ocultar los elementos posicionados debajo de el.**
#### Relative

A diferencia del valor *absolute* este no remueve el elemento del flujo normal del documento, los elementos vecinos respetan el espacio asignado originalmente para contener el elemento. Otra diferencia es que el movimiento del elemento a traves de las propiedades *top*, *bottom*, *right* y *left* o la propiedad *inset* se realiza respecto a su posición original, es decir, a diferencia de *position: absolute* este no busca por un elemento padre respecto del cual moverse. 

**Nota: Al aplicar esta propiedad el elemento se encuentra en una capa superior, por lo que al moverse puede ocultar los elementos posicionados debajo de el.**

```
position: relative;
top: 10px;
```
#### Fixed

Este valor al igual que *absolute* remueve el elemento del flujo normal del documento y los elementos vecinos no guardan un espacio para contenerlo. Este de igual forma admite las propiedades *top*, *bottom*, *right* y *left* o la propiedad *inset* para moverlo de posición, sin embargo, este movimiento se realiza respecto al *viewport*, por lo que siempre estará visible en pantalla.

```
position: fixed;
top: 0;
```
#### Sticky

Este valor permite que el elemento sea parte del flujo normal del documento, las propiedades *top*, *bottom*, *right* y *left* o la propiedad *inset* le indican un margin respecto al borde superior del *viewport*. 

Cuando el movimiento de *scroll* de la página esta por sobrepasar el *margin* el elemento comienza a desplazarse hacia abajo junto con el *scroll* y mientras el borde inferior del elemento padre lo permita. Cuando el movimiento de *scroll* va hacia arriba, el elemento comienza a retornar a su posición original.

**Nota: El desplazamiento del elemento no afecta la posición de los elementos vecinos, pero si los oculta al estar en una capa superior.**

```
position: sticky;
top: 10px;
```

En el ejemplo anterior, el elemento se quedará en su posición original siguiendo el flujo normal del documento, cuando el borde superior del *viewport* este a 10 pixeles el elemento comenzará a moverse verticalmente hacia abajo respetando los 10 pixeles de margen y lo hara en tanto no cruce el borde inferior de su elemento padre. Cuando el *scroll* vaya hacia arriba, el elemento comenzará a seguir el movimiento hasta retornar a su posición original.