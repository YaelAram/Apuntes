## Contexto de Apilamiento

Una página en HTML puede verse como una superposición de varias capas cada una con elementos HTML que al sobreponerse crean las interfaces de usuario que a diario vemos. Esta propiedad nos permite controlar que tan arriba en ese eje *Z* queremos que cierta capa se muestre, lo que puede provocar lo siguiente:

- Una capa con un nivel inferior, ve su contenido oculto cuando los elementos de la capa objetivo pasan sobre ella.
- Una capa con un nivel superior, ve como su contenido oculta los elementos de la capa objetivo cuando estos pasan sobre ella.

Por defecto algunas propiedades en CSS crean una nueva capa para los elementos hijos del elemento padre sobre el cual son aplicadas. Algunas de estas propiedades son:

- El elemento *html*.
- La propiedad *position* con los valores *fixed* o *sticky*.
- La propiedad *position* con los valores *absolute* o *relative* cuando el valor de la propiedad *z-index* es diferente de *auto*.
- Un elemento con un valor del atributo *opacity* menos a uno.
- Un elemento hijo de un contenedor *flex* o *grid* con un valor *z-index* diferente a *auto*.

Para una mayor referencia acerca de estos atributo visitar [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_positioned_layout/Understanding_z-index/Stacking_context)
## Propiedad Z-Index

Esta propiedad nos permite modificar el valor *z-index* de una capa en nuestro diseño. Los posibles valores para este atributo son:

- **Auto**: Este valor no crea un nuevo contexto de apilamiento.
- **Integer**: Este valor no tiene unidad, representa un numero que indica el valor en la coordenada *z*, un numero mayor le indica al navegador que el contenido de la capa tiene una mayor relevancia y viceversa.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index)

**Nota: Por defecto, un elemento muestra en una capa superior su contenido y en una inferior el borde, por lo que ante un desplazamiento del contenido el borde es ocultado debajo del contenido.**