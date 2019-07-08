Installation
========

```bash
$ cp .env.sample .env
$ vim .env # usually, it is not necessary for local develop environment.
$ cp laravel/.env.sample laravel/.env
$ vim laravel/.env # usually, it is not necessary for local develop environment.
$ docker-compose run --rm app composer install
$ docker-compose run --rm app php artisan key:generate
$ docker-compose run --rm app php artisan storage:link
$ docker-compose run --rm app php artisan migrate
```

Launch
========

```bash
$ docker-composer up -d web app db
$ open http://localhost
```
