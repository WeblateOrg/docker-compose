#!/bin/sh

DOCKER_COMPOSE_VERSION=1.22.0

TEMPFILE=`mktemp`
curl -L https://github.com/docker/compose/releases/download/${DOCKER_COMPOSE_VERSION}/docker-compose-`uname -s`-`uname -m` > $TEMPFILE
chmod 755 $TEMPFILE
sudo rm /usr/local/bin/docker-compose
sudo mv $TEMPFILE /usr/local/bin/docker-compose
