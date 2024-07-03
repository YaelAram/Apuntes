El siguiente código nos permite definir variables y poder utilizarlas a lo largo del archivo CSS, lo que nos permite centralizar parte de la lógica.

Fuente [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties)

```
:root {
  --main-bg-color: brown;
}
```

Para poder utilizar el valor de una variable debemos realizar lo siguiente:

```
h1 {
	color: var(--main-bg-color);
}
```