.. image:: https://s.weblate.org/cdn/Logo-Darktext-borders.png
   :alt: Weblate
   :target: https://weblate.org/
   :height: 80px

**Weblate is libre software web-based continuous localization system,
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

1. Clone the docker-compose repository:

   .. code-block:: shell

      git clone https://github.com/WeblateOrg/docker-compose.git
      cd docker-compose

2. Create a ``docker-compose.override.yml`` file with your settings.

   .. code-block:: yml

        version: '3'
        services:
          weblate:
            ports:
              - 80:8080
            environment:
              WEBLATE_SITE_DOMAIN: example.com
              WEBLATE_EMAIL_HOST: smtp.example.com
              WEBLATE_EMAIL_HOST_USER: user
              WEBLATE_EMAIL_HOST_PASSWORD: pass
              WEBLATE_ALLOWED_HOSTS: your hosts
              WEBLATE_ADMIN_PASSWORD: password for admin user

3. Start it up:

   .. code-block:: shell

        docker-compose up

5. For more detailed instructions and configuration visit https://docs.weblate.org/en/latest/admin/install/docker.html

Rebuilding the weblate docker image
-----------------------------------

The `docker-compose` files can be found in https://github.com/WeblateOrg/docker-compose.
The weblate docker image is built from https://github.com/WeblateOrg/docker.
