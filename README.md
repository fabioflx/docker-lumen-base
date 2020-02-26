# Very basic Lumen docker server

[![Downloads](https://img.shields.io/github/downloads/fabioflx/docker-lumen-base/total)](https://github.com/fabioflx/docker-lumen-base)
[![Status](https://img.shields.io/badge/stable-v1.0-blue)]()
[![License](https://img.shields.io/github/license/fabioflx/docker-lumen-base)](https://github.com/fabioflx/docker-lumen-base)

## Description

This is a very easy-to-setup docker configuration you can use to save your time when you need a basic REST server and have no time to waste.

## Usage

Clone the repo, then build it:

`docker-compose build`

Start the container of the server:

`docker-compose up -d`

Access the container:

`docker-compose exec server /bin/bash`

Initialize Lumen:

`/root/.composer/vendor/bin/lumen new site`

Type `exit` to leave the container and you're done.

This will create a **www** folder in your host containing the [Lumen framework](https://lumen.laravel.com) that you can configure according to your needs.

To access the framework just point to http://localhost:80

## License

This repo is open-sourced software licensed under the [MIT license](LICENSE).
