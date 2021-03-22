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
docker stop container_ID
docker rm container_ID
```

- remove:
```bash
docker rm -f container_ID
```

- logs:
```bash
docker logs -f --details container_ID
```

#### Config notes:

**Make working directories:**
mkdir /usr/local/apache2/htdocs /usr/share/nginx/html /var/www/html

**mariadb_phpmyadmin:**

db access: 
- console: mysql -h localhost -P 3306 --protocol=tcp -u root -p
- phpmyadmin: http://localhost:8765/
- phpPDO: host=mariadb

**php_apache_nginx:**

If the project has `public` folder (Laravel, ZF, ...), set `DocumentRoot "/var/www/html/public"` in `./httpd/httpd.conf` and `httpd { server { location { root /var/www/html/public` in `./nginx/nginx.conf`