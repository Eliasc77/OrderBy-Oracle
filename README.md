# OrderBy-Oracle
#### nos sirve para organizar campos en una tabla en un orden especifico

```sql
CREATE TABLE ARTICULOS(
ID_ARTICULO	INT NOT NULL PRIMARY KEY,
ARTICULO VARCHAR2(50) NOT NULL,
COD_FABRICANTE	NUMBER(10) NOT NULL,
);
```

```sql
insert into articulos values(2,'TALADRO WALT',1012546955);
insert into articulos values(3,'ALICATE ACE',1012432365);
insert into articulos values(4,'PALA SENIC',1012345678);
insert into articulos values(5,'TALADRO MILLWAKEE',1012545210);

```

>para ver los registros ordenados utilizando la clausula order by necesitamos definirlo por cual campo queremos que la consulta organice los datos

``` sql
select * from articulos order by id_articulo;
```

| ID_ARTICULO | ARTICULO|COD_FABRICANTE|
|:---:|:-----:|:----:|
|2 | TALADRO WALT' | 1012546955 |
|3 | ALICATE ACE | 1012432365) |
|4 | PALA SENIC | 1012345678 |
|5 | TALADRO MILLWAKEE | 1012545210 |

##### por defaul orderby lo ordena de forma asc
___

``` sql
select * from articulos order by id_articulo desc ;
```
| ID_ARTICULO | ARTICULO|COD_FABRICANTE|
|:---:|:-----:|:----:|
|5 | TALADRO MILLWAKEE | 1012545210 |
|4 | PALA SENIC | 1012345678 |
|3 | ALICATE ACE | 1012432365) |
|2 | TALADRO WALT' | 1012546955 |

___

> otra forma de organizar los campo es colocando el numero del campo correspondiente en la tabla

``` sql
select * from articulos order by 1 desc ;
```
| ID_ARTICULO | ARTICULO|COD_FABRICANTE|
|:---:|:-----:|:----:|
|5 | TALADRO MILLWAKEE | 1012545210 |
|4 | PALA SENIC | 1012345678 |
|3 | ALICATE ACE | 1012432365) |
|2 | TALADRO WALT' | 1012546955 |

##### el 1 indica el primer campo de nuestra tabla = id_articulo
