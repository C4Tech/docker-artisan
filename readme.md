# PHP container for Laravel Artisan services

A basic PHP 5.x CLI container to execute `artisan` commands.


## Configuration

1. `/app` must be a mounted volume and be the Laravel application root.

We use the `c4tech/generic-data` image to provide `app` as a linked volume.
Also, `c4tech/laravel-nginx` is what we use for our PHP-FPM service.

## Docker Compose example

```
artisan:
  image: c4tech/laravel-artisan
  volumes_from:
    - data
```
