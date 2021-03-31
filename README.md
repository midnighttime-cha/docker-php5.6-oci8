# Docker: apache2.4, PHP5.6 connect to Oracle 11g r2 with OCI8

## Clone docker image from Github
```bash
git clone https://github.com/midnighttime-cha/docker-php5.6-oci8.git
cd docker-php5.6-oci8
```

## Build Docker image
```bash
docker build -t docker.pkg.github.com/midnighttime-cha/docker-php5.6-oci8/php5.6-oci8 .
```

## Docker run
```bash
docker run -p 8080:80 -d -v $(pwd)/example:/var/www/html \
--restart=always \
--name php5.6-oci8 \
docker.pkg.github.com/midnighttime-cha/docker-php5.6-oci8/php5.6-oci8
```

## Test
* Open [http://127.0.0.1:8080](http://127.0.0.1:8080) in your browser
