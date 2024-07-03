Esta propiedad CSS nos permite tomar una imagen y realizar zoom sobre ella, mostrando únicamente aquella porción de la imagen que nos interesa.

**Nota: Esta característica aun es experimental.**

Fuente [aquí.](https://ishadeed.com/article/css-object-view-box/)

```
img {
	object-view-box: inset(25% 20% 15% 0%);
}
```

Donde:

- 25% le indica al navegador que debe ignorar el primer 25% de la imagen a partir del borde superior.
- 20% le indica al navegador que debe ignorar el primer 20% de la imagen a partir del borde derecho.
- 15% le indica al navegador que debe ignorar el primer 15% de la imagen a partir del borde inferior.
- 0% le indica al navegador que debe ignorar el primer 0% de la imagen a partir del borde izquierdo.
