*Lanzamiento: Noviembre de 2023*.

Algunas de las características más relevantes introducidas en C# 12 fueron:

- Se introdujo la sintaxis de *primary constructor* con el fin de simplificar la sintaxis en aquellas clases que solo cuenten con un constructor.

```
public class Person(string Name, string LastName, DateOnly Birthday)
{
    public string Name { get; set; } = Name;
    public string LastName { get; set; } = LastName;
    public DateOnly Birthday { get; } = Birthday;
}
```

- Las *lambda functions* ahora pueden ser definidas con parámetros por defecto.

```
var buildGreeting = (string name = "Yael") => $"{name} says hi!";
```

- Se introdujo la posibilidad de concatenar *arrays* utilizando el *spread operator*:

```
int[] row = [1, 2, 3];
int[] column = [4, 5, 6];

int[] table = [..row, ..column];
```

- Se mejoro el patrón de inyección de dependencias, ahora podemos asignar un *token* o *key* a las dependencias que comparten un mismo tipo. Dicho *token* nos permite elegir el servicio que deseamos inyectar.