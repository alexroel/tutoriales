# Instalar MySQL y MySQL Workbench en Ubuntu

## Instalar MySQL
1. Actualizar los repositorios 
2. Instalar MySQL 
    ~~~
    sudo apt-get install mysql-server
    mysql --version
    ~~~
3. Ver manual de MySQL
    ~~~
    man mysql
    ~~~
4. Acceso en local 
    ~~~
    mysql -u root -p
    ~~~
5. Acceso desde otros equipos  
    ~~~
    mysql -h localhost -u root -p
    ~~~

## MySQL Workbench
1. Instalar Workbeanch desd la tienda 
2. Habilitar los permisos para password para workbeanch
3. En MySQL tenemos que dar permisos para dar acceso al usuario root 
    ~~~
    mysql -u root -p
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';
    ~~~
