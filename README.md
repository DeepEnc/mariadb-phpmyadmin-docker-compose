# Mariadb Server and phpMyAdmin with Docker Compose

This Docker Compose configuration sets up a MariaDB server and phpMyAdmin for managing database via a web interface.

## Prerequisites

- Docker

## Usage

1. Clone the repository and navigate to the directory containing the `docker-compose.yml` file in your terminal as below:
```bash
git clone git@github.com:DeepEnc/mariadb-phpmyadmin-docker-compose.git

cd mariadb-phpmyadmin
```
2. Copy ```.env.example``` file to ```.env``` on the same directory as below. Modify the values according to your preference.
```bash
cp .env.example .env
``` 
3. However, if values are not modified, default values in the ```docker-compose.yml``` file will be taken as input.

4. Run the following command to start the services:
```
docker compose up -d
```

5. Once the services are running, you can access phpMyAdmin by opening a web browser and navigating to [http://localhost:8080](http://localhost:8080). If you modify the ```PHPMYADMIN_PORT``` on ```.env``` file then use the defined port rather than 8080.

6. Log in to phpMyAdmin using the credentials defined in ```.env``` file. By default:
```
user: user
password: password
```
7. You can now manage your MariaDB databases using phpMyAdmin.

8. Run the following command to check whether the containers are running or not
```
docker ps
```
It should display two containers running. 

9. Run the following command to stop the services:
```
docker compose down 
``` 

## Customization

- You can customize the MariaDB root password, database name, user, password, and port number in the ```.env``` file.
