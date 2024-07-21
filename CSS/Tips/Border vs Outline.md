Ambas propiedades se encargar de crear un contorno al rededor de nuestro elemento, sin embargo, estos tienen una sutil diferencia:

- La propiedad *border* crear un contorno y lo inserta dentro del contenedor del elemento HMTL, por lo que puede provocar cambios en el layout de la página, como saltos o desplazar elementos.
- La propiedad *outline* crea un contorno y lo dibuja sobre el espacio del contenedor del elemento HTML, por lo que no provoca cambios en el layout de la página.

```
/* Este provoca un ligero cambio en el layout */
button:hover {
	border: 1px solid black;
}

/* Este mantiene el layout de la página */
button:hover {
	outline: 1px solid black;
}
```