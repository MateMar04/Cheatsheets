# SQL
SQL proviene de Structured Query Language que en español se traduce como Lenguaje de Consulta Estructurado. Es un lenguaje de programación diseñado para gestionar y manipular bases de datos relacionales. SQL permite a los usuarios almacenar, recuperar, actualizar y eliminar datos de las bases de datos. Proporciona una forma estandarizada de interactuar con las bases de datos y se utiliza ampliamente en el campo de la gestión de datos.

SQL es un lenguaje declarativo, lo que significa que los usuarios especifican qué quieren recuperar o modificar sin necesariamente especificar cómo hacerlo. Permite a los usuarios definir la estructura de una base de datos usando tablas, columnas y relaciones, y realizar varias operaciones en los datos dentro de esas bases de datos.

Es compatible con muchos sistemas de gestión de bases de datos (DBMS) como MySQL, Oracle Database, Microsoft SQL Server, PostgreSQL y SQLite. Si bien existen variaciones en la sintaxis y las características de SQL en diferentes sistemas de bases de datos, los conceptos y principios fundamentales siguen siendo los mismos.


## DDL
DDL significa Data Definition Language, que en español se traduce como Lenguaje de Definición de Datos. Los comandos DDL se usan para definir la estructura y las características de los objetos de la base de datos. Estos comandos no afectan directamente a los datos en sí, sino que se enfocan en la creación y modificación de la estructura de la base de datos.

- *CREATE:* Se usa para crear objetos en la base de datos, como tablas, vistas, índices, procedimientos almacenados, etc.
- *ALTER:* Permite realizar modificaciones en la estructura de los objetos existentes en la base de datos, como agregar, modificar o eliminar columnas en una tabla, cambiar el nombre de un objeto, etc.  
- *DROP:* Se usa para eliminar objetos de la base de datos, como tablas, vistas, índices, etc.  
- *TRUNCATE:* Permite eliminar todos los registros de una tabla, pero mantiene la estructura de la tabla intacta.  
- *RENAME:* Permite cambiar el nombre de un objeto en la base de datos, como renombrar una tabla o una columna.


## DML
DML significa Data Manipulation Language, que en español se traduce como Lenguaje de Manipulación de Datos. Es un conjunto de comandos usados en SQL para manipular y operar sobre los datos almacenados en una base de datos relacional. Los comandos DML se centran en la manipulación y modificación de los datos almacenados en la base de datos. A diferencia de los comandos DDL que se usan para definir la estructura de la base de datos, los comandos DML se utilizan para interactuar con los datos y realizar operaciones de inserción, actualización, eliminación y recuperación en las tablas.

- *SELECT*: Se utiliza para recuperar datos de una o varias tablas. Permite especificar las columnas que se desean obtener, aplicar condiciones de filtrado y realizar operaciones de unión y agrupación.  
- *INSERT:* Permite insertar nuevos registros en una tabla. Se especifica qué valores se deben ingresar para cada columna correspondiente al nuevo registro.  
- *UPDATE:* Se utiliza para modificar los datos existentes en una o varias filas de una tabla. Permite cambiar los valores de una o varias columnas en función de ciertas condiciones.
- *DELETE:* Permite eliminar uno o varios registros de una tabla. Se pueden especificar condiciones para filtrar los registros a eliminar.

## DCL
DCL significa Data Control Language, que en español se traduce como Lenguaje de Control de Datos. Es un conjunto de comandos utilizados en SQL para administrar los permisos y privilegios de acceso a los objetos de la base de datos.


### TIPOS DE DATOS

#### Strings

|  Syntax | Maximum Size                                     | Explanation                                                                                                                   |
|------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| CHAR(size)       | Maximum size of 255 characters.                  | Where size is the number of characters to store. Fixed-length strings. Space padded on right to equal size characters.        |
| VARCHAR(size)    | Maximum size of 65,535 characters.                  | Where size is the number of characters to store. Variable-length string.                                                      |
| TINYTEXT(size)   | Maximum size of 255 characters.                  | Where size is the number of characters to store.                                                                              |
| TEXT(size)       | Maximum size of 65,535 characters.               | Where size is the number of characters to store.                                                                              |
| MEDIUMTEXT(size) | Maximum size of 16,777,215 characters.           | Where size is the number of characters to store.                                                                              |
| LONGTEXT(size)   | Maximum size of 4GB or 4,294,967,295 characters. | Where size is the number of characters to store.                                                                              |
| BINARY(size)     | Maximum size of 255 characters.                  | Where size is the number of binary characters to store. Fixed-length strings. Space padded on right to equal size characters. |
| VARBINARY(size)  | Maximum size of 255 characters.                  | Where size is the number of characters to store. Variable-length string.                                                      |

#### Numericos

|  Syntax      | Maximum Size                                                                                                                | Explanation                                                                                                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BIT(m)                | Where m goes from 1 to 64. Default is 1.                                                  | Numbers represented in bits e.g. BIT(5) type with value b'00111' is the numeric value 7.                                                                                                                        |
| TINYINT(m)            | Signed values range from -128 to 127. Unsigned values range from 0 to 255.                                                  | Very small integer value.                                                                                                                                                         |
| SMALLINT(m)           | Signed values range from -32768 to 32767. Unsigned values range from 0 to 65535.                                            | Small integer value.                                                                                                                                                              |
| MEDIUMINT(m)          | Signed values range from -8388608 to 8388607. Unsigned values range from 0 to 16777215.                                     | Medium integer value.                                                                                                                                                             |
| INT(m)                | Signed values range from -2147483648 to 2147483647. Unsigned values range from 0 to 4294967295.                             | Standard integer value.                                                                                                                                                           |
| INTEGER(m)            | Signed values range from -2147483648 to 2147483647. Unsigned values range from 0 to 4294967295.                             | Standard integer value. This is a synonym for the INT datatype.                                                                                                                   |
| BIGINT(m)             | Signed values range from -9223372036854775808 to 9223372036854775807. Unsigned values range from 0 to 18446744073709551615. | Big integer value.                                                                                                                                                                |
| DECIMAL(m,d)          |                                                                                                                             | Unpacked fixed point number. m defaults to 10, if not specified.  d defaults to 0, if not specified. Where m is the total digits and d is the number of digits after the decimal. |
| DEC(m,d)              |                                                                                                                             | This is a synonym for the DECIMAL datatype.                                                                                                                                       |
| NUMERIC(m,d)          |                                                                                                                             | This is a synonym for the DECIMAL datatype.                                                                                                                                       |
| FIXED(m,d)            |                                                                                                                             | Unpacked fixed-point number. Where m is the total digits and d is the number of digits after the decimal. (Introduced in MySQL 4.1). This is a synonym for the DECIMAL datatype.  |
| FLOAT(m,d)            |                                                                                                                             | Single precision floating point number. Where m is the total digits and d is the number of digits after the decimal.                                                              |
| DOUBLE(m,d)           |                                                                                                                             | Double precision floating point number. Where m is the total digits and d is the number of digits after the decimal.                                                              |
| DOUBLE PRECISION(m,d) |                                                                                                                             | This is a synonym for the DOUBLE datatype.                                                                                                                                        |
| REAL(m,d)             |                                                                                                                             | This is a synonym for the DOUBLE datatype.                                                                                                                                        |
| FLOAT(p)              |                                                                                                                             | Floating point number. Where p is the precision.                                                                                                                                  |
| BOOL                  |                                                                                                                             | Treated as a boolean data type where a value of 0 is considered to be FALSE and any other value is considered to be TRUE. Synonym for TINYINT(1)                                  |
| BOOLEAN               |                                                                                                                             | This is a synonym for the BOOL datatype.                                                                                                                                          |


#### Fecha / Tiempo

|  Syntax | Maximum Size                                                          | Explanation                       |
|------------------|-----------------------------------------------------------------------|-----------------------------------|
| DATE             | Values range from 1000-01-01 to 9999-12-31.                           | Displayed as YYYY-MM-DD.          |
| DATETIME         | Values range from 1000-01-01 00:00:00 to 9999-12-31 23:59:59.         | Displayed as YYYY-MM-DD HH:MM:SS. |
| TIMESTAMP(m)     | Values range from 1970-01-01 00:00:01 UTC to 2038-01-19 03:14:07 UTC. | Displayed as YYYY-MM-DD HH:MM:SS. |
| TIME             | Values range from -838:59:59 to 838:59:59.                            | Displayed as HH:MM:SS.            |
| YEAR[(2 or 4)]      | Year value as 2 digits or 4 digits.                                   | Default is 4 digits.              |


#### Large Object (LOB)

| Syntax | Maximum Size                                     | Explanation                                                                                        |
|------------------|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| TINYBLOB         | Maximum size of 255 bytes.                       |                                                                                                    |
| BLOB(size)       | Maximum size of 65,535 bytes.                    | Where size is the number of characters to store (size is optional and was introduced in MySQL 4.1) |
| MEDIUMBLOB       | Maximum size of 16,777,215 bytes.                |                                                                                                    |
| LONGTEXT         | Maximum size of 4GB or 4,294,967,295 characters. |                                                                                                    |




### Crear base de datos

``` sql
DROP DATABASE IF EXISTS [database_name];
CREATE DATABASE IF NOT EXISTS [database_name];
USE [database_name];
```

### Crear Tablas

``` sql
CREATE TABLE [table_name]
(
	[pk | INT AUTO_INCREMENT PRIMARY KEY],
    [field_name | data_type],
    [CONSTRAINT [constraint_name] FOREIGN KEY ([column_name]) REFERENCES [table_name] (table_column)]
);
```

### Alterando Tablas

#### Agregar clave primaria

``` sql
ALTER TABLE table_name
  ADD CONSTRAINT [ constraint_name ]
    PRIMARY KEY [ USING BTREE | HASH ] (column1, column2, ... column_n)
```

Ejemplo:
``` sql
ALTER TABLE contacts
  ADD CONSTRAINT contacts_pk
    PRIMARY KEY (last_name, first_name);
```

#### Agregar Columna

``` sql
ALTER TABLE table_name
  ADD new_column_name column_definition
    [ FIRST | AFTER column_name ];
```

Ejemplo:
``` sql
ALTER TABLE contacts
  ADD last_name varchar(40) NOT NULL
    AFTER contact_id;
```

#### Modificar tipo de dato de una columna

``` sql
ALTER TABLE table_name
  MODIFY column_name column_definition
    [ FIRST | AFTER column_name ];
```

Ejemplo:
``` sql
ALTER TABLE contacts
  MODIFY last_name varchar(50) NULL;
```

#### Eliminar columna

``` sql
ALTER TABLE table_name
  DROP COLUMN column_name;
```


#### Renombrar columna

``` sql
ALTER TABLE table_name
  CHANGE COLUMN old_name new_name 
    column_definition
    [ FIRST | AFTER column_name ]
```

Ejemplo:
``` sql
ALTER TABLE contacts
  CHANGE COLUMN contact_type ctype
    varchar(20) NOT NULL;
```


#### Agregar clave foránea

``` sql
ALTER TABLE contacts
  ADD
[CONSTRAINT [symbol]] FOREIGN KEY
    [index_name] (index_col_name, ...)
    REFERENCES tbl_name (index_col_name,...)
    [ON DELETE reference_option]
    [ON UPDATE reference_option]
```

Ejemplo:
``` sql
CREATE TABLE products
( product_name VARCHAR(50) NOT NULL,
  location VARCHAR(50) NOT NULL,
  category VARCHAR(25),
  CONSTRAINT products_pk PRIMARY KEY (product_name, location)
);

CREATE TABLE inventory
( inventory_id INT PRIMARY KEY,
  product_name VARCHAR(50) NOT NULL,
  location VARCHAR(50) NOT NULL,
  quantity INT,
  min_level INT,
  max_level INT
);

ALTER TABLE inventory ADD 
  CONSTRAINT fk_inventory_products
    FOREIGN KEY (product_name, location)
    REFERENCES products (product_name, location);
```




### Insertando Datos
 
 ``` sql
 INSERT INTO [table_name] (columns)
 VALUES [(values, ...)],
		[(values, ...)],
		[(values, ...)];
```

Ejemplo

``` sql
INSERT INTO FILM (TITLE, DESCRIPCION, RELEASE_YEAR)
VALUES ('The Shawshank Redemption',
        'Two imprisoned men bond over a number of years, finding solace and eventual redemption through acts of common decency.',
        '1994-09-22'),
       ('The Godfather', 'An organized crime dynasty transfers control from father to son.', '1972-03-24'),
       ('The Dark Knight',
        'When the menace known as the Joker wreaks havoc and chaos on the people of Gotham, Batman must accept one of the greatest psychological and physical tests of his ability to fight injustice.',
        '2008-07-18'),
       ('Pulp Fiction',
        'The lives of two mob hitmen, a boxer, a gangster and his wife, and a pair of diner bandits intertwine in four tales of violence and redemption.',
        '1994-05-21'),
       ('Forrest Gump',
        'The presidencies of Kennedy and Johnson, the events of Vietnam, Watergate, and other historical events unfold through the perspective of an Alabama man with an IQ of 75, whose only desire is to be reunited with his childhood sweetheart.',
        '1994-07-06');
```


### Seleccionando datos

``` sql
SELECT A1, A2, A3..., An
FROM T1, T2, T3,..., Tn
WHERE condition
```

Ejemplo:
``` sql
SELECT title, rating, length
FROM film
WHERE length > 100;
```

#### Operadores en la cláusula where

| Comparison Operator | Description                                           |
|---------------------|-------------------------------------------------------|
| =                   | Equal                                                 |
| <=>                 | Equal (MySql, safe to compare NULL values)            |
| <>                  | Not Equal                                             |
| !=                  | Not Equal                                             |
| >                   | Greater Than                                          |
| >=                  | Greater Than or Equal                                 |
| <                   | Less Than                                             |
| <=                  | Less Than or Equal                                    |
| BETWEEN             | Within a range (inclusive)                            |
| NOT                 | Negates a condition                                   |
| IS NULL             | NULL value                                            |
| IS NOT NULL         | Non-NULL value                                        |
| LIKE                | Pattern matching with % and _                         |
| IN ( )              | Matches a value in a list                             |
| EXISTS              | Condition is met if subquery returns at least one row |

#### Between

```sql
SELECT title, `length` FROM film
WHERE `length` BETWEEN 100 AND 120;
```

#### Multiples tablas

```sql
SELECT city, district
FROM address, city
WHERE address.city_id = city.city_id;
```

``` sql
SELECT FIRST_NAME, LAST_NAME
FROM ACTOR
         INNER JOIN FILM_ACTOR FA ON ACTOR.ACTOR_ID = FA.ACTOR_ID
         INNER JOIN FILM F ON FA.FILM_ID = F.FILM_ID
WHERE F.TITLE = 'ZOOLANDER FICTION';
```

#### Disctinct
Se utiliza junto con el comando SELECT para retornar únicamente los valores distintos de una columna o combinación de columnas en los resultados de una consulta. Esto significa que los valores duplicados se eliminan y solo se muestra una instancia de cada valor único.

``` sql
SELECT DISTINCT columna1, columna2, ...
FROM tabla;
```

Devuelve:
| id | Nombre | Ciudad |
|----|----------|---------|
| 1 | Candela | Barcelona |
| 2 | Mateo | Madrid |
| 3 | Luciana | Madrid |
| 4 | Lorenzo | San Fransisco |


``` sql
SELECT DISTINCT Ciudad
FROM empleados;
```

Devuelve:
| | Ciudad |
|--|------|
| 1 | Barcelona |
| 2| Madrid |
|3| San Francisco |


#### Order by

```sql
SELECT title, special_features, rental_rate, name
 FROM film, film_category, category
WHERE film.film_id = film_category.film_id 
  AND film_category.category_id = category.category_id
ORDER BY rental_rate DESC
```

```sql
SELECT title, special_features, rental_rate, name
 FROM film, film_category, category
WHERE film.film_id = film_category.film_id 
  AND film_category.category_id = category.category_id
ORDER BY rental_rate DESC, special_features ASC
```

#### Limit
La cláusula LIMIT en SQL se utiliza para restringir el número de filas que se devuelven en los resultados de una consulta. Permite limitar la cantidad de registros que se muestran, lo cual es útil cuando se trabaja con grandes conjuntos de datos o cuando solo se necesita un subconjunto específico de los resultados.

``` sql
SELECT *
FROM clientes
LIMIT 5;
```

Esto nos devolvería los primeros 5 registros de la tabla "clientes".

#### Like
La cláusula LIKE en SQL se utiliza para buscar patrones dentro de los valores de una columna en una consulta. Permite realizar búsquedas de texto basadas en patrones utilizando caracteres especiales conocidos como comodines.

-   El símbolo '%' representa cualquier secuencia de cero o más caracteres.
-   El símbolo '_' representa cualquier carácter individual.

``` sql
SELECT *
FROM clientes
WHERE nombre LIKE 'J%';
```
Esto nos devolvería todos los registros de la tabla "clientes" donde el nombre comienza con "J".

``` sql
SELECT *
FROM clientes
WHERE nombre LIKE '_a%';
```
Esto nos devolvería todos los registros de la tabla "clientes" donde el nombre tiene una "a" en la segunda posición.

#### Aritmética

```sql
SELECT title, description, rental_rate * 150 AS "In Pesos" 
FROM film
```

### Union
La cláusula UNION en SQL se utiliza para combinar el resultado de dos o más consultas en un solo conjunto de resultados. Permite fusionar filas de resultados de consultas distintas en una única tabla virtual resultante.

``` sql
SELECT last_name FROM actor  
UNION  
SELECT last_name FROM actor;
```
Esto devolverá una fila con el apellido de los actores, por más que haya muchos actores con el mismo apellido

``` sql
SELECT last_name FROM actor  
UNION ALL
SELECT last_name FROM actor;
```
Esto devolverá el apellido de cada actor

``` sql
select title from film  
UNION  
select last_name from actor;
```
Esto devolverá una sola columna con los títulos de las películas y luego los apellidos de los actores

### Variables de las Tablas

``` sql
SELECT f.title, f.special_features, f.rental_rate, c.name
 FROM film f, film_category fc,  category c 
WHERE f.film_id = fc.film_id 
  AND fc.category_id = c.category_id
ORDER BY f.rental_rate DESC, f.special_features ASC
```
Las variables son f, fc y c


### Subqueries en el WHERE

#### IN
```sql
SELECT DISTINCT first_name,last_name 
  FROM customer,payment 
 WHERE customer.customer_id = payment.customer_id 
   AND payment.amount BETWEEN 3 AND 4; 
```

```sql
SELECT first_name,last_name 
  FROM customer 
 WHERE customer_id IN (SELECT customer_id 
                         FROM payment 
                        WHERE amount BETWEEN 3 AND 4); 
```
Estas dos queries devuelven todos los clientes distintos que pagaron entre 3 y 4, nada más que en una se usa el IN y una subquery y en la otra el DISTINCT y el AND.

``` sql
SELECT first_name,last_name  
FROM customer,payment  
WHERE customer.customer_id = payment.customer_id  
AND payment.amount BETWEEN 3 AND 4;
```
En cambio, esta devuelve todos los clientes que hayan pagado entre 3 y 4 veces. Puede aparecer varias veces el mismo cliente.


```sql
SELECT DISTINCT first_name 
  FROM customer,payment 
 WHERE customer.customer_id = payment.customer_id 
   AND payment.amount = 0.99 
   AND first_name LIKE ( 'W%' ) 
 ORDER BY first_name; 
```

```sql
SELECT first_name 
  FROM customer 
 WHERE customer_id IN (SELECT customer_id 
                         FROM payment 
                        WHERE amount = 0.99) 
   AND first_name LIKE ( 'W%' ) 
 ORDER BY first_name; 
```
En este caso hay que usar subqueries o reformular la primera query, ya que la primera nos dará un mal resultado porque devolverá todos los nombres distintos, por lo que si hay dos clientes con el mismo nombre pero distinto apellido serán absorbidos por el distinct.

La query correcta sin la subquery sería:

``` sql
SELECT DISTINCT customer.customer_id, first_name  
FROM customer,  
payment  
WHERE customer.customer_id = payment.customer_id  
AND payment.amount = 0.99  
AND first_name LIKE ('W%')  
ORDER BY first_name;
```

#### Except como subquery

```sql
SELECT first_name, last_name 
  FROM customer 
 WHERE customer_id IN (SELECT customer_id 
                         FROM payment 
                        WHERE amount = 0.99) 
   AND customer_id NOT IN (SELECT customer_id 
                             FROM payment 
                            WHERE amount = 1.99) 
   AND first_name LIKE ( 'W%' ) 
```

``` sql
SELECT first_name, last_name  
FROM customer  
WHERE customer_id IN (SELECT customer_id  
FROM payment  
WHERE amount = 0.99)  
AND first_name LIKE ('W%')  
EXCEPT  
SELECT first_name, last_name  
FROM customer  
WHERE customer_id IN (SELECT customer_id  
FROM payment  
WHERE amount = 1.99);
```
(La cláusula except se agregó en mysql 8.0.31)

#### Exists
La cláusula EXISTS en SQL se utiliza para verificar si existe al menos una fila que cumple una determinada condición en una subconsulta. Esta cláusula devuelve un valor booleano (verdadero o falso) en función de si la subconsulta devuelve algún resultado o no.

``` sql
SELECT first_name,last_name 
  FROM customer c1 
 WHERE EXISTS (SELECT * 
                 FROM customer c2 
                WHERE c1.first_name = c2.first_name 
                  AND c1.customer_id <> c2.customer_id); 
```
Esta devuelve todos los clientes distintos que comparten el mismo nombre

``` sql
SELECT title,`length`  
FROM film f1  
WHERE NOT EXISTS (SELECT *  
FROM film f2  
WHERE f2.`length` > f1.`length`);
```
Esta devuelve todas las películas que tienen la mayor duración

#### ALL / ANY
La cláusula ALL en SQL se utiliza para comparar un valor con todos los valores de un conjunto resultante de una subconsulta. Devuelve verdadero si la condición se cumple para todos los valores en el conjunto y falso si al menos uno de los valores no cumple la condición.

``` sql
SELECT title, length  
FROM film  
WHERE length >= ALL (SELECT length  
FROM film);
```
Esta devuelve todas las películas que tienen la mayor duración

``` sql
SELECT *
FROM productos
WHERE precio > ALL (SELECT precio_promedio
                    FROM precios_promedio);
```
Esta query devuelve todos los productos cuyo precio sea mayor al promedio.


La cláusula ANY en SQL se utiliza para comparar un valor con al menos uno de los valores en un conjunto resultante de una subconsulta. Devuelve verdadero si la condición se cumple para al menos uno de los valores en el conjunto y falso si ninguno de los valores cumple la condición.

``` sql
-- Films whose replacement cost is higher than the lowest replacement cost 
SELECT title, replacement_cost 
  FROM film 
 WHERE replacement_cost > ANY (SELECT replacement_cost 
                                 FROM film) 
 ORDER BY replacement_cost; 

-- Same query with exists
 SELECT title, replacement_cost 
  FROM film f1 
 WHERE EXISTS (SELECT * 
                 FROM film f2 
                WHERE f1.replacement_cost > f2.replacement_cost) 
 ORDER BY replacement_cost; 
 ```


### Subqueries en el FROM

``` sql
SELECT title,description,
rental_rate,
rental_rate * 150 AS in_pesos 
  FROM film 
 WHERE rental_rate * 150 > 10.0 
   AND rental_rate * 150 < 70.0;
```

``` sql
SELECT * 
  FROM (SELECT title,description,rental_rate,rental_rate * 150 AS in_pesos 
          FROM film) g 
 WHERE in_pesos > 10.0 
   AND in_pesos < 70.0; 
```
Estas dos queries son equivalentes

### Subqueries en el SELECT

``` sql
SELECT customer_id,  
first_name,  
last_name,  
(SELECT DISTINCT amount  
FROM payment  
WHERE customer.customer_id = payment.customer_id  
AND amount >= ALL (SELECT amount  
FROM payment  
WHERE customer.customer_id = payment.customer_id))  
AS max_amount  
FROM customer  
ORDER BY max_amount DESC,  
customer_id DESC;  
```

``` sql
SELECT customer_id,  
first_name,  
last_name,  
(SELECT MAX(amount)  
FROM payment  
WHERE payment.customer_id = customer.customer_id) AS max_amount  
FROM customer  
ORDER BY max_amount DESC,  
customer_id DESC;  
```

``` sql
SELECT customer.customer_id,  
first_name,  
last_name,  
MAX(amount) max_amount  
FROM customer,  
payment  
WHERE customer.customer_id = payment.customer_id  
GROUP BY customer_id, first_name, last_name  
ORDER BY max_amount DESC, customer_id DESC
```
Estas tres queries son equivalentes


### Aggregations

- MIN() devuelve el menor valor de la columna seleccionada.

``` sql
SELECT MIN(amount)
  FROM customer, payment
 WHERE customer.customer_id = payment.customer_id
   AND customer.last_name LIKE 'R%'
```

- MAX() devuelve el mayor valor de la columna seleccionada.

``` sql
SELECT MAX(amount)
  FROM customer, payment
 WHERE customer.customer_id = payment.customer_id
   AND customer.last_name LIKE 'R%'
```

- COUNT() devuelve la cantidad de filas que cumplen con ciertos requisitos.

``` sql
SELECT COUNT(*)
  FROM inventory
  WHERE store_id = 1;
```

- AVG() devuelve el valor promedio de la columna numerica seleccionada.

``` sql
SELECT AVG(amount)
  FROM customer, payment
 WHERE customer.customer_id = payment.customer_id
   AND customer.last_name LIKE 'R%'
```

- SUM() devuelve el valor total de la columna numerica seleccionada.

``` sql
SELECT SUM(amount)
  FROM customer, payment
 WHERE customer.customer_id = payment.customer_id
   AND customer.last_name LIKE 'R%'
```

### Group by
La cláusula GROUP BY en SQL se utiliza para agrupar filas de una tabla según un criterio específico y aplicar funciones de agregación a esas filas agrupadas. Permite realizar operaciones de resumen y obtener resultados basados en grupos de datos en lugar de en filas individuales.

``` sql
-- Find films amounts per rating
SELECT rating, COUNT(*)
  FROM film
 GROUP BY rating

-- Find films durations per rating
SELECT rating, AVG(length)
  FROM film
 GROUP BY rating
 ```


#### Having
La cláusula HAVING en SQL se utiliza junto con la cláusula GROUP BY para filtrar los resultados de una consulta basada en una condición que involucra las funciones de agregación. A diferencia de la cláusula WHERE, que se aplica a las filas antes de agruparlas, la cláusula HAVING se aplica después de la agrupación y se utiliza para filtrar grupos de filas resultantes.


``` sql
-- Find customers that rented only one film
SELECT c.customer_id, first_name, last_name, COUNT(*)
  FROM rental r1, customer c
 WHERE c.customer_id = r1.customer_id
GROUP BY c.customer_id, first_name, last_name
HAVING COUNT(*) = 1
```

### Operaciones de Conjuntos

[Imgur](https://imgur.com/nccypto)


``` sql
SELECT *  
FROM film  
WHERE NOT EXISTS(SELECT * FROM inventory WHERE film.film_id = inventory.film_id);
```
Todas las peliculas que no esten en el inventario


<hr>

![[3.png]]
``` sql
SELECT *  
FROM film  
WHERE EXISTS(SELECT * FROM inventory WHERE film.film_id = inventory.film_id);
```
Todas las peliculas que esten en el inventario.

<hr>

![[5.png]]

``` sql
SELECT *  
FROM film, inventory;
```