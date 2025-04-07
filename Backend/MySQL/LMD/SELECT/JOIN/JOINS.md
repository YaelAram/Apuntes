![[join-sql.jpg]]

```
select CAMPOS from TABLA_1 ALIAS_1 TIPO_JOIN TABLA_2 ALIAS_2 on ALIAS_1.COLUMNA_1 = ALIAS_2.COLUMNA_2;
```

Donde:

- **CAMPOS**: Indica los campos a incluir en la consulta, estos deben hacer referencia a la tabla que pertenecen ya sea por su nombre o alias, *NOMBRE_TABLA.NOMBRE_COLUMNA*.
- **TABLA_1**: Indica el nombre de la primer tabla.
- **ALIAS_1**: Indica el alias de la primer tabla.
- **TIPO_JOIN**: Indica que tipo de join se debe llevar a cabo.
	- INNER JOIN
	- LEFT JOIN
	- RIGHT JOIN
	- CROSS JOIN / FULL OUTER JOIN
- **TABLA_2**: Indica el nombre de la segunda tabla.
- **ALIAS_2**: Indica el alias de la segunda tabla.
- **COLUMNA_1**: Indica el nombre de la columna de la primer tabla que sirve como enlace a la segunda.
- **COLUMNA_2**: Indica el nombre de la columna de la segunda tabla que sirve como enlace a la primera.

Ejemplo:

```
select u.name, s.state_name from users u inner join states s on u.id_state = s.id;
```

Ejemplo, con uniendo tres tablas (la tabla principal es la primera en ser escrita):

```
select u.name, s.state_name, b.balance from users u inner join states s on u.id_state = s.id (inner join bank b on u.bank_account = b.account);
```

## NATURAL JOIN

Es una variante en la cual el sistema gestor de la base de datos busca en las tablas a relacionar dos atributos que coincidan en el nombre y tipo da dato para realizar el enlace entre ambas tablas.

```
select CAMPOS from TABLA_1 ALIAS_1 natural join TABLA_2 ALIAS_2;
```

Donde:

- **CAMPOS**: Indica los campos a incluir en la consulta, estos deben hacer referencia a la tabla que pertenecen ya sea por su nombre o alias, *NOMBRE_TABLA.NOMBRE_COLUMNA*.
- **TABLA_1**: Indica el nombre de la primer tabla.
- **ALIAS_1**: Indica el alias de la primer tabla.
- **TIPO_JOIN**: Indica que tipo de join se debe llevar a cabo.
	- INNER JOIN
	- LEFT JOIN
	- RIGHT JOIN
	- CROSS JOIN / FULL OUTER JOIN
- **TABLA_2**: Indica el nombre de la segunda tabla.
- **ALIAS_2**: Indica el alias de la segunda tabla.

Ejemplo:

```
select u.name, s.state_name from users u natural join states s;
```