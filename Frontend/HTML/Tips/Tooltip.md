Un tooltip permite mostrar información que puede orientar al usuario da pequeñas descripciones sobre el funcionamiento de algún elemento o aclara un concepto.

Fuente [Midudev](https://x.com/midudev/status/1790762819731804349)

```
<button style="anchor-name: --anchor" popovertarget="tooltip">
	<p aria-hidden="true">?</p>
</button>

<div id="tooltip" class="tooltip" style="position-anchor: --anchor" popover>
	<p>Contenido del tooltip</p>
</div>
```

En CSS realizamos lo siguiente:

```
.tooltip {
	inset-area: bottom;
}
```

Donde:

- Utilizamos el atributo *ancho-name* en el elemento *button* y el atributo *position-anchor* en el *div* para enlazar ambos elementos.
- El atributo *popover* convierte al elemento *div* en un *popover element* lo que le agrega ciertas propiedades, por ejemplo, su atributo *display* es igualado a *none* y este permanece oculto hasta que un elemento *button* con el atributo *popovertarget* lo invoque o a traves de la llamada del método *popoverElement.showPopover()*.
- El atributo *popovertarget* del elemento *button* permite ocultar (cuando el usuario no tiene el cursor sobre el elemento) o mostrar un elemento *popover* (cuando el usuario tiene el cursor sobre el elemento). Este atributo debe recibir el mismo valor que el del atributo *id* del elemento *popover*.
- Con la propiedad CSS *inset-area* controlamos el lugar donde aparece el tooltip.
