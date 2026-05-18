# Tasks API + Events

## Stack
- Laravel
- PHP 8.4
- Redis Queue
- Docker
- MySQL

## Run

```bash
docker compose up -d --build
docker compose exec app composer install
docker compose exec app php artisan migrate
docker compose exec app php artisan key:generate
```

## Start queue worker

```bash
docker compose up queue
```

## Send ping jobs

```bash
docker compose exec app php artisan queue:ping
```

## Publish outbox

```bash
docker compose exec app php artisan outbox:publish
```

## Retry failed jobs

```bash
docker compose exec app php artisan queue:retry all
```

## Logs
- storage/logs/laravel.log
- storage/logs/failed.log
