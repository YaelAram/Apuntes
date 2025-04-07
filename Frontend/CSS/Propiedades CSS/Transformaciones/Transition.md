Esta propiedad es un atajo para las propiedades *transition-delay*, *transition-duration*, *transition-property* y *transition-timing-function*. Nos permite definir una transición entre dos estados de un elemento, estos estados están definidos por el estilo por defecto de un elemento y el estilo a aplicar al elemento modificado por un pseudo clase.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/transition)

Si solo se indica en el estilo por defecto, la configuración se aplicara en la transición de ida y vuelta.

```
transition: scale 4s; /* Propiedad Duracion */
transition: scale 4s 1s; /* Propiedad Duracion Delay */
transition: scale 4s ease-in; /* Propiedad Duracion Timing */
transition: scale 4s ease-in 1s; /* Propiedad Duracion Timing Delay */

/* Es posible configurar dos transiciones a la vez */
transition: scale 4s ease-in 1s, box-shadow 2s ease-out 1s;
```

Si se indica de la siguiente forma, podemos indicar una configuración para la transición de ida y otra configuración para la transición de vuelta, donde la propiedad *transition* del estilo por defecto configura la transición de *vuelta* y la del estilo *hover* la transición de *ida*.

```
button {
	background: blue;
	transition: background 300ms ease-in; /* Hover -> Normal */
}

button:hover {
	background: red;
	transition: background 500ms ease-in; /* Normal -> Hover */
}
```
## Accesibilidad

Existe un *media query* que detecta si el usuario ha configurado su navegador para deshabilitar las animaciones y efectos, podemos utilizarla para hacer nuestra aplicación amigable con esos usuarios.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/@media/prefers-reduced-motion)

```
@media(prefers-reduced-motion: reduce) {
	button {
		transition: none;
	}
}
```
## Transition-Property

Esta propiedad nos permite indicar la propiedad sobre la cual deseamos crear una transición.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-property)

**Nota: Considerar que una transición puede ser definida sobre una propiedad si esta tiene uno o varios estados intermedios, como el cambia de un color a otro o de un tamaño a otro.**

```
transition-property: scale;
```
## Transition-Duration

Nos permite indicar el tiempo que deberá tardar el elemento en cambiar de un estado a otro.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration)

Esta propiedad admite como unidad de tiempo el segundo "s" o el milisegundo "ms".

```
transition-duration: 500ms;
```
## Transition-Delay

Nos permite indicar el tiempo que debe esperar el elemento antes de iniciar la transición.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-delay)

Esta propiedad admite el mismo tipo de valores que la propiedad *transition-duration*.
## Transition-Timing-Function

Esta propiedad nos permite indicar a CSS como debe calcular los valores intermedios de la transición.

Referencia [MDN.](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-timing-function)

Esta propiedad admite los siguientes valores:

- **Ease**: Este es el valor por defecto. En este modo la transición se acelera en la primera mitad para alentarse en la segunda mitad.
- **Linear**: La transición es igual de rápida a lo largo de su duración.
- **Ease-In**: La transición inicia lento y se acelera hasta su fin.
- **Ease-Out**: La transición inicia rápido y desacelera hasta su fin.
- **Ease-In-Out**: La transición inicia lento, acelera y termina lento.
- **Cubic-Bezier**: Esta es una función que nos permite definir como debe CSS calcular los estados intermedios.

**Nota: Las herramientas de desarrollo en el apartado CSS y en la linea sobre la cual definimos la propiedad *transition* o *transition-timing-function* nos ofrecen un editor con el cual podemos diseñar nuestra función *cubic-bezier*.**