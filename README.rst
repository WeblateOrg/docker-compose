.. image:: https://s.weblate.org/cdn/Logo-Darktext-borders.png
   :alt: Weblate
   :target: https://weblate.org/
   :height: 80px

**Weblate is a copylefted libre software web-based continuous localization system,
used by over 2500 libre projects and companies in more than 165 countries.**

The docker-compose for Docker container for Weblate

.. image:: https://readthedocs.org/projects/weblate/badge/
    :alt: Documentation
    :target: https://docs.weblate.org/en/latest/admin/install/docker.html

Documentation
-------------

Detailed documentation is available in Weblate documentation:

https://docs.weblate.org/en/latest/admin/install/docker.html

Getting started
---------------

1. Create a `docker-compose.override.yml` file with your settings.

   .. code-block:: yml

        version: '3'
        services:
          weblate:
            image: weblate/weblate
            ports:
              - 80:8080
            environment:
              WEBLATE_EMAIL_HOST: smtp.example.com
              WEBLATE_EMAIL_HOST_USER: user
              WEBLATE_EMAIL_HOST_PASSWORD: pass
              WEBLATE_ALLOWED_HOSTS: your hosts
              WEBLATE_ADMIN_PASSWORD: password for admin user

2. Build the instances

        docker-compose build

3. Start up

        docker-compose up

4. For more detailed instructions visit https://docs.weblate.org/en/latest/admin/install/docker.html

Rebuilding the weblate docker image
-----------------------------------

The `docker-compose` files can be found in https://github.com/WeblateOrg/docker-compose.
The weblate docker image is built from https://github.com/WeblateOrg/docker.
