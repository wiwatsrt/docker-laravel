# Docker Laravel

[![Build Status](https://travis-ci.org/wiwatsrt/docker-laravel.svg?branch=master)](https://travis-ci.org/wiwatsrt/docker-laravel)

Laravel development environment in Docker Containers

### Installing Laravel Via Composer Create-Project

```
$ docker-compose run --rm composer create-project --prefer-dist laravel/laravel .
```

### Configure Laravel for mysql
change `DB_HOST` in `.env` to point to `mysql`.

### Running Artisan commands

```
Example:
$ docker-compose run --rm artisan make:auth
$ docker-compose run --rm artisan migrate
$ docker-compose run --rm artisan tinker
```

### Running composer commands
```
Example:
$ docker-compose run --rm composer update
$ docker-compose run --rm composer require laravelcollective/html
```

### Nodejs

```
$ docker-compose run --rm nodejs npm install
```

### Gulp

```
Example:
$ docker-compose run --rm nodejs gulp install
$ docker-compose run --rm nodejs gulp
$ docker-compose run --rm nodejs gulp watch
```