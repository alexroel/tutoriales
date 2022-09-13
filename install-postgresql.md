# Instalar PostgreSQL en Ubuntu 

## Instalar PostgreSQL 
Con este comando se descargará y se instalara en su ultima versión. 

~~~bash
sudo apt-get -y install postgresql postgresql-contrib
~~~

Ingrese a PostgreSQL con el siguiente comando 
~~~bash
sudo su - postgres

psql
~~~

Crea el usuario y la contraseña para administrar bases de datos  con PostgreSQL. 

~~~bash
create user alexroel with password '123456';
~~~

Dar permisos de super usuario a `alexroel`.
~~~bash
alter user alexroel with superuser;
~~~
## Crear tu primer base de datos con PostgreSQL 
Podemos crear nuestro primer base de datos con el siguiente comando para el usuario `alexroel`. 

~~~bash
create database tutorial_db owner alexroel; 
~~~ 

Listar base de datos. 
~~~bash
\l

\list
~~~

Para salir
~~~bash
exit
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










