# Introduction

Docker-compose file and application settings for the Mailpit server installation and configuration.

[Mailpit](https://github.com/axllent/mailpit) Mailpit is a small, fast, low memory, zero-dependency, multi-platform email testing tool & API for developers.

# Development with Docker

## Docker installation

A working [Docker](https://docs.docker.com/engine/installation/) installation is mandatory.

### Docker environment variables file

Please make sure to copy & rename the **example.env** file to **.env**.

``cp env.example .env``

You can replace the values if needed to match you server & environment. Mainly the path to the SQLite database and the path to the authentication file.

### Build & run

Build & run all the containers for this project.

``docker-compose up -d``

### Frontends

To access the main application please use the following link.

http://localhost:8484

# Deployment with Docker

Copy and rename the environment file.

``cp example.env .env``

You should replace the values since the default ones are not ready for production.

Please also make sure to copy & rename the **docker-compose.override.yml.prod** file to **docker-compose.override.yml**.

`cp docker-compose.override.yml.prod docker-compose.override.yml`

You can replace the values if needed, but the default ones should work for production.

Build & run all the containers for this project:

`docker-compose up -d`

Use a reverse proxy configuration to map the url to port `8484`.
Example configurations are included in [proxy examples](https://mailpit.axllent.org/docs/configuration/proxy).
