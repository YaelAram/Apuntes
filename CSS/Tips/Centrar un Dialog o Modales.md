Los siguientes estilos CSS son especialmente útiles para centrar vertical y horizontalmente un elemento dentro del *viewport* de la página, por lo que es ideal para elementos que se posicionan por encima del contenido principal de la página (como un modal o *dialog*).

```
position: absolute;
inset: 0;
margin: auto;
```

**Nota: Para lograr que el elemento quede al centro del *viewport* no debe estar dentro de un elemento con el atributo *position: relative* ya que este se centraría respecto al elemento en cuestión y no respecto al *viewport*.**