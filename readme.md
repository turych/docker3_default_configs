**Make working directories:**
mkdir /usr/local/apache2/htdocs /usr/share/nginx/html


**docker commands:**
- run project:
```bash
docker-compose up # run
docker-compose up --build # rebuild config and run
docker-compose up --build # rebuild config and run background
```
- show docker process list:
 ```bash
docker ps
```
```
CONTAINER ID        IMAGE       ...
988e27da7bdf        httpd:2.4   ...
```

- stop and remove container:
```bash
docker stop 988e27da7bdf
docker rm 988e27da7bdf
```

- remove:
```bash
docker rm -f 988e27da7bdf
```

####Config notes:

*Make working directories:*
mkdir /usr/local/apache2/htdocs /usr/share/nginx/html

**mariadb_phpmyadmin:**
mysql: mysql -h localhost -P 3306 --protocol=tcp -u root -p
phpmyadmin: http://localhost:8765/

