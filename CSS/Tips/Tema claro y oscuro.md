## Utilizando un media query

Este media query nos permite realizar cambios en nuestra página dependiendo del tema del sistema operativo del usuario.

```
@media(prefers-color-scheme: dark) {
	body {
		background: black;
		color: white;
	}
}
```
## Ajustar el valor de una propiedad según el tema

Esta función nos permite elegir entre dos valores dependiendo del tema actual.

Fuente [Midudev.](https://x.com/midudev/status/1714228713074655420)

**Nota: Es una característica que aun no es soportada por todos los navegadores.**

```
h1 {
	color: light-dark(black, white);
}
```