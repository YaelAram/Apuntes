Nos permite agrupar un conjunto de elementos de un formulario, rodearlos con un borde y darles un titulo de grupo.

Fuente [MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset)

```
<form>
	<fieldset>
		<legend>Datos Personales</legend>
		<input type="text" placeholder="Nombre de Usuario" />
		<input type="email" placeholder="Correo Electronico" />
	</fieldset>
</form>
```

Una característica relevante es que si establecemos el atributo *disabled* en *true* todos los elementos de formulario que contiene el elemento *fieldset* son deshabilitados.