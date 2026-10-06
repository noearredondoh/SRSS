## Descripción

Connect to this PostgreSQL server and find the flag! `psql -h xebec.cylabacademy.net -p 44403 -U postgres pico`

Password is `postgres`

What does a SQL database contain?

## Solución

```
┌──(jeex㉿LAPTOP-77F4GRAK)-[~]
└─$ psql -h xebec.cylabacademy.net -p 44403 -U postgres pico
Password for user postgres:

Y ingresamos la contraseña : postgres


pico=# \dt
          List of tables
 Schema | Name  | Type  |  Owner
--------+-------+-------+----------
 public | flags | table | postgres
(1 row)


Solo tenemos una tabla... flags

pico-# \d flags
                        Table "public.flags"
  Column   |          Type          | Collation | Nullable | Default
-----------+------------------------+-----------+----------+---------
 id        | integer                |           | not null |
 firstname | character varying(255) |           |          |
 lastname  | character varying(255) |           |          |
 address   | character varying(255) |           |          |
Indexes:
    "flags_pkey" PRIMARY KEY, btree (id)

regresamos
pico=# ^C


y colocamos
pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | academy{L3arN_S0m3_5qL_t0d4Y_d4538dde}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 rows)



```

```
academy{L3arN_S0m3_5qL_t0d4Y_412c85d9}
```

## Notas adicionales

\dt Muestra las tablas de la base de datos. \d tabla Muestra las columnas y estructura de una tabla. SELECT * FROM tabla; Muestra todos los datos de una tabla. \l Muestra las bases de datos disponibles.
## Referencias