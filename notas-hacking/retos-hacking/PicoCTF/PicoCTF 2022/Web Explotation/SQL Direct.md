
## Descripción
Connect to this PostgreSQL server and find the flag!

## Solución
Hay que extraer la bandera de la base de datos en la tabla flags
``` bash
┌─[dantefx@dantefx-Inspiron5481]─[~]
└──╼ $psql -h saturn.picoctf.net -p 50425 -U postgres pico
Contraseña para usuario postgres: 
psql (13.5 (Debian 13.5-0+deb11u1), servidor 14.2 (Debian 14.2-1.pgdg110+1))
ADVERTENCIA: psql versión mayor 13, servidor versión mayor 14.
          Algunas características de psql podrían no funcionar.
Digite «help» para obtener ayuda.

pico=# \l
pico=# \c pico
psql (13.5 (Debian 13.5-0+deb11u1), servidor 14.2 (Debian 14.2-1.pgdg110+1))
ADVERTENCIA: psql versión mayor 13, servidor versión mayor 14.
          Algunas características de psql podrían no funcionar.
Ahora está conectado a la base de datos «pico» con el usuario «postgres».
pico=# \dt
        Listado de relaciones
 Esquema | Nombre | Tipo  |  Dueño   
---------+--------+-------+----------
 public  | flags  | tabla | postgres
(1 fila)

pico=# SELECT * FROM flags;
 id | firstname | lastname  |                address                 
----+-----------+-----------+----------------------------------------
  1 | Luke      | Skywalker | picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
  2 | Leia      | Organa    | Alderaan
  3 | Han       | Solo      | Corellia
(3 filas)

pico=# 


```
picoCTF{L3arN_S0m3_5qL_t0d4Y_21c94904}
