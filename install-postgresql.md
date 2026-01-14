# Instalar PostgreSQL en Ubuntu 

## Instalar PostgreSQL 
Con este comando se descargará y se instalara en su ultima versión. 

~~~bash
sudo apt-get -y install postgresql postgresql-contrib
~~~

Comprobar la versión instalada de PostgreSQL.
~~~bash
psql --version
~~~

Ingrese a PostgreSQL con el siguiente comando 
~~~bash
sudo -i -u postgres
psql
~~~

Crea el usuario propio y la contraseña para administrar bases de datos  con PostgreSQL. 

~~~sql
CREATE USER alexroel WITH PASSWORD '123456';
~~~

- Esta es una contraseña de ejemplo, se recomienda usar una contraseña segura.

Dar permisos de super usuario a `alexroel`.
~~~sql
ALTER USER alexroel WITH superuser;
~~~

Ahora crea una base de datos con el mismo nombre de usuario `alexroel`. Para poder administrar la base de datos con el usuario creado.

~~~sql
CREATE DATABASE alexroel OWNER alexroel;
\du
~~~

Salir de PostgreSQL
~~~sql
\q
exit
~~~

## Crear tu primer base de datos con PostgreSQL 
Podemos crear nuestro primer base de datos con el siguiente comando para el usuario `alexroel`. 

Primero ingresamos con el usuario creado.
~~~bash
psql -U alexroel -h localhost 
~~~ 

Listar base de datos. 
~~~bash
\l

\list
~~~

Ahora creamos una base de datos llamada `tutos_db`.
~~~sql
CREATE DATABASE tutos_db;
~~~

Usar la base de datos creada.
~~~sql
\c tutos_db
~~~

Ahora puedes crear tablas de ejemplo dentro de la base de datos `tutos_db`.
~~~sql
CREATE TABLE usuarios (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(100)
);
~~~

Listar tablas creadas.
~~~sql
\dt
~~~

Para salir de PostgreSQL.
~~~sql
\q
~~~

## Instalar PgAdmin 
Para instalar PgAdmin nesecitaremos `curl` y lo podemos instalar con el siguiente comando. 

~~~bash
sudo apt install curl 
~~~


Instale la clave pública para el repositorio (si no lo hizo previamente):

~~~bash
sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
~~~

Cree el archivo de configuración del repositorio:

~~~bash
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
~~~


Instalar pgAdmin, instalar para los modos de escritorio y web:
~~~bash
sudo apt install pgadmin4
~~~

## Ejecutar PgAdmin4 
Buscas en tus aplicaciónes logo de PgAdmin o PotgreSQL, luego colocas los credenciales. a `Add New Server`,  

- En general Nombre de sevidor. 
- En Connection Host; `localhost`  el pueto pordefecto. 
- En Username `alexroel` y `password`










