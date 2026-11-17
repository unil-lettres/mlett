# Introduction

Docker configuration and application settings for the Mailpit server. This is used internally by the Faculty of Arts IT-Web team.

[Mailpit](https://github.com/axllent/mailpit) is a small, fast, low memory, zero-dependency, multi-platform email testing tool & API for developers.

# Development with Docker

## Docker installation

A working [Docker](https://docs.docker.com/engine/installation/) installation is mandatory.

## Environment files

Please make sure to copy & rename the **example.env** file to **.env**.

``cp env.example .env``

You can replace the values if needed to match you server & environment. Mainly the path to the SQLite database and the path to the authentication file.

Make sure to copy & rename the **docker-compose.override.yml.dev** file to **docker-compose.override.yml**.

``cp docker-compose.override.yml.dev docker-compose.override.yml``

You can replace the values if needed, but the default ones should work for local development.

## Installation & configuration

Build & run all the containers for this project.

``docker compose up`` (add -d if you want to run in the background and silence the logs)

## Frontends

To access the main application please use the following link.

http://localhost:8484

# Deployment with Docker

## Environment files

Copy and rename the environment file.

``cp env.example .env``

You should replace the values since the default ones are not ready for production.

Make sure to copy & rename the **docker-compose.override.yml.prod** file to **docker-compose.override.yml**.

`cp docker-compose.override.yml.prod docker-compose.override.yml`

You can replace the values if needed, but the default ones should work for production.

## Installation & configuration

Build & run all the containers for this project.

`docker compose up -d`

## Reverse proxy

Use a reverse proxy configuration to map the url to port `8484`. Configuration examples can be found at [https://mailpit.axllent.org/docs/configuration/proxy](https://mailpit.axllent.org/docs/configuration/proxy).
