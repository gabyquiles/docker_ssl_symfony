# docker_ssl_symfony
Docker setup to run a symfony project with SSL

This setup allows to run a symfony project in docker with SSL. In order to use two files need to be modified.
- docker-compose.yml
- docker/nginx/symfony2.conf 

Replace server_name for the url to be used, host_ip for the ip of the host machine, mysql_database for the new database name. In order to autoimport sql files you can add them to docker/mysql_setup/data.
