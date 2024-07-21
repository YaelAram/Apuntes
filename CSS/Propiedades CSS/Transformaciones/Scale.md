Esta propiedad nos permite escalar un elemento.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/scale)

Esta propiedad admite los siguientes valores:

- **Porcentaje**: Permite indicar el factor de escalado en forma de porcentaje, siendo 100% el tamaño original del elemento.
- **Numero**: Este permite indicar el factor de escalado de la siguiente manera, un numero menos a 1 provoca que el elemento se encoja mientras que uno mayor provoca que el elemento aumente de tamaño.

**Nota: Un aspecto relevante de esta propiedad es que no provoca un movimiento del layout ya que para el documento el elemento nunca cambia de tamaño, es decir, el cambio de tamaño es únicamente visual.**

```
scale: 1.2; /* Aumenta el tamaño un 20% en el eje X y Y */

/* Aumenta el tamaño un 50% en el eje X y lo reduce a un 50% en el eje Y */
scale 1.5 50%;
```