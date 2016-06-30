Composer for PHP5 with PostgreSQL driver.
======

Basic Usage
------

```
docker run -v $(pwd):/app \
    webridge/composer \
    install
```

Link to a PostgreSQL Database
------
```
docker run --name db_name -d postgresql

docker run \
    -v $(pwd):/app \
    --link db_name:db \
    webridge/composer \
    install
```

Keeping Cache
------

```
docker run \
    -v $(pwd):/app \
    -v /local/path/to/.composer:/root/.composer \
    -e COMPOSER_HOME=/root/.composer \
    webridge/composer \
    install
```

You may also add composer parameters after `install` such as `--prefer-dist`.

Symfony
------

If you are building a `Symfony 3.*` project, you may wanna add an extra environment variable:

```
    -e SENSIOLABS_ENABLE_NEW_DIRECTORY_STRUCTURE=true \
```