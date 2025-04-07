*Lanzamiento: Noviembre de 2022*.

Algunas de las características más relevantes introducidas en C# 11 fueron:

- Se agrego el modificador *required* el cual le indica al compilador que las propiedades marcadas como *required* deben de ser inicializadas antes del que el objeto pueda ser utilizado.

```
public required string Name { get; set; }
public required string Birthday { get; init; }
```

- Se agrego el modificador de acceso *file* el cual únicamente permite el acceso a los objetos, funciones, etc que se encuentren en el mismo archivo de código fuente.
- Se mejoro la posibilidad de interpolar variables en *raw string literals*.

```
string nombre = "Yael";
int edad = 25;

string texto = $"""
Hola, mi nombre es {nombre}.
Tengo {edad} años.
Esto es un ejemplo de raw string literal con variables interpoladas.
""";

Console.WriteLine(texto);
```