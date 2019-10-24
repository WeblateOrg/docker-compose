# weblate-docker-compose

[![Build Status](https://travis-ci.com/WeblateOrg/docker-compose.svg?branch=master)](https://travis-ci.com/WeblateOrg/docker-compose)
[![Documenation](https://img.shields.io/readthedocs/weblate.svg)](https://docs.weblate.org/en/latest/admin/install/docker.html)

The docker-compose for Docker container for Weblate

## Documentation

Detailed documentation is available in Weblate documentation:

https://docs.weblate.org/en/latest/admin/install/docker.html

## Getting started

1. Create a `docker-compose.override.yml` file with your settings.

    ```yml
    version: '2'
    services:
      weblate:
        ports:
          - 80:8080
        environment:
          WEBLATE_EMAIL_HOST: smtp.example.com
          WEBLATE_EMAIL_HOST_USER: user
          WEBLATE_EMAIL_HOST_PASSWORD: pass
          WEBLATE_ALLOWED_HOSTS: your hosts
          WEBLATE_ADMIN_PASSWORD: password for admin user
    ```

2. Build the instances

        docker-compose build

3. Start up

        docker-compose up

4. For more detailed instructions visit https://docs.weblate.org/en/latest/admin/install/docker.html

## Rebuilding the weblate docker image

The `docker-compose` files can be found in https://github.com/WeblateOrg/docker-compose.
The weblate docker image is built from https://github.com/WeblateOrg/docker.
