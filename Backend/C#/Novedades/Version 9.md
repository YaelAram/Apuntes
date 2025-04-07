*Lanzamiento: Noviembre de 2020*.

Algunas de las características más relevantes introducidas en C# 9 fueron:

- Se creo el modificador *init* el cual de estar presente convierte a la propiedad de una clase en inmutable (una vez creado el objeto su valor no podrá ser modificado). Si este modificador esta presente no podrá usarse el *set*.

```
public string Name {get; init;} = name;
```

- C# 8: Se simplifico la sintaxis al crear un objeto si durante la definición de la variable ya se especifico el tipo de la variable. En esta versión se mejoro el soporte de dicha sintaxis para que pueda ser utilizada durante la creación de colecciones.

```
List<Person> people = new();
```

- Se introdujo soporte para las *record class* las cuales nos permite almacenar información en tipos de datos inmutables.

```
public record Post(
    int UserId,
    int? Id,
    string Title,
    string Body
);
```

- Se creo la *keyword with* la cual nos permite crear una nueva instancia de una *record class* pero modificando los valores que necesitemos:

```
var post = new Post(1, 1, "Hello", "World");
var post1 = post with { Title = "Goodbye" };
```

- El *pattern matching* de la sentencia *switch* recibe mejoras permitiéndonos validar rangos de valores.
- Se introdujo soporte para los *high level programs* los cuales nos permiten ejecutar lógica en nuestro archivo principal sin la necesidad de envolverlo en un *namespace* y una clase. Nos permite un inicio rápido en programas cuya complejidad sea mínima.