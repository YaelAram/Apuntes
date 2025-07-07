*Lanzamiento: Noviembre de 2024*.

Algunas de las características más relevantes introducidas en C# 13 fueron:

- La *keyword params* ahora permite especificar el tipo de colección que deseamos usar para recibir los parámetros:

```
void PrintNames(params string[] names)
{
	foreach(var name in names)
	{
		Conssole.WriteLine(name);
	}
}

PrintNames("Yael", "Juan", "Oscar");
```

- Ahora podemos utilizar la indexación inversa para asignar nuevos valores a dichas posiciones:

```
numeros[^1] = 5;
```

- Se mejora el proceso mediante el cual el lenguaje decide que método mandar a llamar según los parámetros y el contexto en el que se esta ejecutando.