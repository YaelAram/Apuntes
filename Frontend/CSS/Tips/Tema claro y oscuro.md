### Utilizando un media query

Este media query nos permite realizar cambios en nuestra página dependiendo del tema del sistema operativo del usuario.

```
@media(prefers-color-scheme: dark) {
	body {
		background: black;
		color: white;
	}
}
```
### Ajustar el valor de una propiedad según el tema

Esta función nos permite elegir entre dos valores dependiendo del tema actual.

Fuente [Midudev.](https://x.com/midudev/status/1714228713074655420)

**Nota: Es una característica que aun no es soportada por todos los navegadores.**

```
h1 {
	color: light-dark(black, white);
}
```
### Ajustar SVG al tema de la aplicación

Podemos ajustar las propiedades de un SVG como el color de relleno o de contorno dentro del propio archivo *.svg* agregando una etiqueta *style* con las propiedades de color y contorno, además del *media query prefers-color-scheme*.


```
<svg
  xmlns="http://www.w3.org/2000/svg"
  fill="currentColor"
  viewBox="0 0 128 128">		
  <path d="..." />

  <style>
    svg { color: #000; }

	@media(prefers-color-scheme: dark) {
	  svg { color: #fff; }
	}
  </style>

</svg>
```