# Instalar MySQL y MySQL Workbench en Ubuntu

## Instalar MySQL
1. Actualizar los repositorios 
2. Instalar MySQL 
    ~~~bash
    sudo apt-get install mysql-server
    mysql --version
    ~~~
3. Ver manual de MySQL
    ~~~bash
    man mysql
    ~~~
4. Acceso en local  
    ~~~bash
    mysql -u root
    ~~~
5. Configuración de usuario y contraseña  
    ~~~bash
    CREATE USER 'alexroel'@'localhost' IDENTIFIED BY '123456';
    ~~~
6. Otorgar todos los privilegios al nuevo usuario:
    ~~~bash
    GRANT ALL PRIVILEGES ON *.* TO 'alexroel'@'localhost' WITH GRANT OPTION;
    ~~~

## MySQL Workbench
1. Instalar Workbeanch desd la tienda 
2. Habilitar los permisos para password para workbeanch
3. En MySQL tenemos que dar permisos para dar acceso al usuario root 
    ~~~
    mysql -u root
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';
    ~~~

## Crear base de datos 
Para crear una base de datos en MySQL, puedes seguir los siguientes pasos:

- Paso 1: Iniciar sesión en MySQL como usuario root o con otro usuario:
~~~bash
mysql -u root -p    #Para usuario root
mysql -u alexroel -p # Para otro  usuario 
~~~
- Paso 2: Listar base de datos.

~~~bash
SHOW DATABASES;

+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.00 sec)
~~~

- Paso 3: Crear la base de datos:

~~~bash
CREATE DATABASE todolist_db;
~~~

- Paso 4: Verificar la creación de la base de datos:

~~~bash
SHOW DATABASES;

+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
| todolist_db        |
+--------------------+
5 rows in set (0.00 sec)
~~~



