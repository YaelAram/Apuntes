*Lanzamiento: Noviembre de 2021*.

Algunas de las características más relevantes introducidas en C# 10 fueron:

- Se introdujo la característica *global usings* los cuales importan por defecto algunos de los *namespaces* más utilizados con el fin de reducir ligeramente la cantidad de lineas de de código en nuestros archivos.

Archivo *.csproj*:

```
// Habilitar los global usings por defecto
<ImplicitUsings>enable</ImplicitUsings>

// Definir un nuevo global using
<ItemGroup>
	<Using Include="System.Threading" />
</ItemGroup>
```

- *Namespaces* por fichero nos permite eliminar un nivel de identación provocado por la definición del *namespace*. Si deseamos definir más de un *namespace* en un fichero debemos utilizar la sintaxis clásica.

```
// Clasica
namespace Fundamentos
{
	public class Person {...}
}

// Nueva
namespace Fundamentos;

public class Person {...}
```

- Se agregaron los tipos de datos *TimeOnly* y *DateOnly*.
- Se agrego la colección *PriorityQueue*.
- Se agregaron los métodos *Min*, *MinBy*, *Max* y *MaxBy* en LINQ con el fin de obtener el menor y mayor elemento de una colección de datos según el criterio proporcionado.
- Se introdujo el método *Chunk* el cual nos permite dividir una colección de datos en segmentos de un tamaño especifico.
- Se agrego soporte al método *Take* de LINQ para la notación de rangos:

Ejemplo, omitir primeros 10 y tomar 15 elementos:

```
// Antes
people.Skip(10).Take(15);
people.Take(10..25);
```

- Se simplifico la definición de una *record class*, la definición de sus propiedades estará dada por el tipo y nombre de los parámetros del constructor.

```
//Antes
public record Post
{
	public string Title { get; init; }
	public bool Done { get; init; }

	public Post(string title, bool done)
	{
		Title = title;
		Done = done;
	}
}

// Ahora
public record Post(string Title, bool Done);
```