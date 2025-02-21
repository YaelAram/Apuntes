Algunas veces es necesario crear un menu desplegable con el fin de facilitar el uso de nuestra barra de navegación en pantallas pequeñas como las de un *smartphone*, este tipo de menú nos permite ocultar nuestra barra de navegación y hacerla visible únicamente cuando el usuario la necesita, estos usualmente reacomodan los elementos del *navbar* en sentido vertical para aprovechar al máximo la pantalla del *smartphone*.

En nuestro HTML definimos lo siguiente:

```
<button popovertarget="aside-nav" type="button">
  Open Modal
</button>

<aside popover="auto" id="aside-nav">
  <menu>...</menu>

  <button popovertarget="aside-nav" type="button" aria-label="Close Menu">
    Close Modal
  </button>
</aside>
```

Mientras que en CSS realizamos lo siguiente:

```
#aside-nav {
  background: #333;
  border: 0;
  color: white;
  position: fixed;
  top: 0;
  left: 0;
  inset: auto;
  height: 100dvh;
  box-shadow: 0 0 25px 25px rgb(0 0 0 / 0.1);
  width: 250px;

  transition: translate 0.2s ease-in-out;
  transition-behavior: allow-discrete;

  &:popover-open {
    @starting-style {
      display: block;
      translate: -100% 0;
    }
  }
}
```