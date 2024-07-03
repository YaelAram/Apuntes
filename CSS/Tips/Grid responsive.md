El siguiente código nos permite crear un grid responsive, mostrando tantos elementos sean posibles en cada fila según el espacio en pantalla del dispositivo.

```
.grid {
	display: grid;
	grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
	gap: 16px;
}
```