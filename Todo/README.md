# Todo-php
# Docker Tutorial
First we need to create a <b>docker-compose.yml</b> file and a <b>Dockerfile</b>. The given two are made with specific network and volumes where the apache is installed through <b>php:7.4-apache</b> with the needed packages for running. These dependencies are mentioned in the Dockerfile. In the docker-compose.yml file, the <b>mysql:latest</b> image was taken and for apache it was build with the help of the Dockerfile. To connect with the backend we only need to change two files, the database_connection.php and the database.php file. The host will be named as per the name of the database container name. We need to copy the file of the git directly in to the ```var/www/html/``` folder and the sql file needs to be in ```var/lib/mysql/``` folder. This can easily be done by copying them in the volume created. Now in order to dump the database entries into the created but empty database the following code has to written: 

```mysql -u root -p simple_todo < simple_todo.sql```
Then we need to need to go to the ip of the main vm or machine with the given port of the web-container.

## A simple Todo list in php and mysql to understand basic of crud operation in php and mysql

 Install wamp or xampp and create a database with the name simple_todo and import simple_todo.sql

 clone your Todo folder to htdocs in case of xampp otherwise to www in case of wamp start apache and mysql

 and you would be able to access it through (https://localhost/Todo/todo.php).


````
