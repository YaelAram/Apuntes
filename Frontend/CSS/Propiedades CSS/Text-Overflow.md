Nos permite indicar al navegador como debe indicarle al usuario que el texto que esta viendo ha sido ocultado debido a que desbordo el elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/text-overflow)

Algunos de los posibles valores de esta propiedad son:

- **Clip**: Este es el valor por defecto. Muestra tanto texto sea posible, llegado al limite simplemente oculta el texto que desborda el elemento. Puede dejar palabras a la mitad.
- **Ellipsis**: Muestra tanto texto sea posible, una vez llegue a los limites del elemento muestra una elipsis "..." poco antes del final para indicar al usuario que el contenido ha sido recortado. Debido a que la elipsis forma parte del *contenido* la cantidad de texto que un elemento puede mostrar es ligeramente menor.

```
text-overflow: ellipsis;
```