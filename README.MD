
## Laravel Docker Nginx PHP-FPM OP_CACHE

Course Videos: https://www.youtube.com/@ahtcloud

Website: https://ahtcloud.com

Laravel Docker Nginx build using PHP-FPM and OP_CACHE.

This build delivers top performance.

By using nginx, php-fpm and op_cache, were able to reduce our request response times and serve requests in `5ms`!




## How to use?

Step 1: Create a new Laravel project

Step 2: Run `git init`

Step 3: Pull this repo `git pull https://github.com/emad-zaamout/laravel-docker-nginx-php-fpm-opcache`

Step 4: Adjust your env variables. Make sure you set your database env vars. Add any values as the database will be created per your env var values.
````
# Adjust your .env variables.

DB_CONNECTION=mysql
DB_HOST=database
DB_PORT=3306
DB_DATABASE=default
DB_USERNAME=laravel
DB_PASSWORD=secret

REDIS_HOST=redis
REDIS_PASSWORD=secret
REDIS_PORT=6379
````

Step 5:
    To run the containers, please use the provided Makefile. Run `make` to see all supported commands.
````
    Usage:
      make <target>

    Targets:
      help        Print help.
      ps          Show containers.
      build       Build all containers for DEV
      build-prod  Build all containers for PROD
      start       Start all containers
      fresh       Destroy & recreate all uing dev containers.
      fresh-prod  Destroy & recreate all using prod containers.
      stop        Stop all containers
      restart     Restart all containers
      destroy     Destroy all containers
      ssh         SSH into PHP container
      install     Run composer install
      migrate     Run migration files
      migrate-fresh  Clear database and run all migrations
      tests       Run all tests
      tests-html  Run tests and generate coverage. Report found in reports/index.html
```

To run all containers for local development, run `make fresh`. Otherwise `make fresh-prod` for prod builds.

Default PHP port is configured to 98000. Connect via `http:/localhost:9000` or `http://127.0.0.1:9000`

Default DB port is 3306.



