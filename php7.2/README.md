# PHP-FPM

## Build

```sh
docker build -t [image name]:[tag name] .
```

## Run

```sh
docker run -d --rm --name [container name] \
    -v www.conf:/usr/local/etc/php-fpm.d/www.conf -v app_path:/app \
    -p 9000:9000 \
    [image name]:[tag name]
```

## Restart

```sh
docker container restart [container name]
```
