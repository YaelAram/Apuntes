*Lanzamiento: Septiembre de 2019*.

Algunas de las características más relevantes introducidas en C# 8 fueron:

- La capacidad de marcar una variable como *nullable*, es decir, su valor puede ser nulo o del tipo de la variable.

```
int? numer = null;
```

- Se agrego una sintaxis que permite realizar *slicing* sobre los elementos de una colección.

```
lista[0..2];
lista[2..];
lista[..2];
```

- Se agrego la capacidad de *pattern matching* a la sentencia *switch*.
- Se simplifico la sintaxis al crear un objeto si durante la definición de la variable ya se especifico el tipo de la variable.

```
// Antes
Person person = new Person("Yael");

// Ahora
Person person = new("Yael");
```

- Ahora es posible definir un comportamiento por defecto a los métodos definidos por una interfaz.