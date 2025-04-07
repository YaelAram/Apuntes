Un *Data Transfer Object* nos permite transformar y validar la información recibida a un objeto adecuado para la acción que quiere ejecutar el usuario.

Definimos el tipo de respuesta de nuestro DTO:

```
type CreateTodoDtoResult = { ok: false; error: string } | 
  { ok: true; todo: { title: string } };
```

Creamos una función que se encargue de validar y generar nuestro DTO:

```
const createTodo = (body: { [key: string]: any }): CreateTodoDtoResult => {
  const { title } = body;

  if (typeof title !== 'string') {
    return { ok: false, error: 'Title field must be a string (required)' };
  }

  if (title.length === 0) {
    return { ok: false, error: 'Title field could not be an empty string' };
  }

  return { ok: true, todo: { title } };
};

export const TodoDto = { createTodo };
```

Utilizamos nuestro DTO:

```
const todoDtoResult = TodoDto.createTodo(req.body);
if (!todoDtoResult.ok) return res.status(400).json({ msg: todoDtoResult.error });
```

