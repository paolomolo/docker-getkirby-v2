# Docker for Kirby CMS (v2)

Dockerfile for a container running Kirby CMS, Alpine, Apache and PHP7

[![Docker Pulls][docker-pulls-src]][docker-pulls-href]
[![Docker Build Status][docker-build-src]][docker-build-href]

Kirby 2 is deprecated. For the latest Dockerfile check out [docker-getkirby-v3](https://github.com/paolomolo/docker-getkirby-v3)

## Getting Started

### Usage with docker-compose

Create a `docker-compose.yml` in your Kirby directory:

``` yaml
version: '2'
services:
  docker:
    image: paolomolo/getkirby-apache:v2
    volumes:
      - ./content:/var/www/localhost/htdocs/content
      - ./site:/var/www/localhost/htdocs/site
      - ./assets:/var/www/localhost/htdocs/assets
    ports:
      - 80:80

```

Then run `docker-compose up` from your command line and visit `localhost` in your browser.

## Built With

* [Kirby CMS (v2)](https://github.com/getkirby-v2) a file‑based CMS
* [Alpine](https://github.com/alpinelinux) a security-oriented, lightweight Linux distribution
* [PHP7](https://github.com/php) incl. `php-curl, php-dom, php-openssl, php-xml, php-json`
* [Apache2](https://github.com/apache) web server

<!-- Badges -->
[docker-pulls-src]: https://img.shields.io/docker/pulls/paolomolo/getkirby-apache?cacheSeconds=21600&color=blue
[docker-pulls-href]: https://hub.docker.com/r/paolomolo/getkirby-apache

[docker-build-src]: https://img.shields.io/docker/build/paolomolo/getkirby-apache?cacheSeconds=21600&label=build
[docker-build-href]: https://hub.docker.com/r/paolomolo/getkirby-apache/builds
