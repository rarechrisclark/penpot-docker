# Penpot Docker

This repository contains a Dockerised setup of [Penpot](https://github.com/penpot/penpot), an open-source design and prototyping platform. The setup includes the Penpot frontend, backend, exporter, PostgreSQL database, Redis cache, and Mailcatcher for SMTP.

## Prerequisites

- Docker
- Docker Compose

## Local Development

*Note: Ensure you have completed the steps outlined in the [Initial Setup](#initial-setup)*

1. Start the containers with `docker compose up -d`
2. The Penpot frontend will be availabe at http://penpot.docker

## Initial Setup

*Note: You will have to add `127.0.0.1   penpot.docker` to your `/etc/hosts` file*

1. Clone this repository to your local machine with `git clone https://github.com/rarechrisclark/penpot-docker.git`
2. Enter the project with `cd penpot-docker`
3. Create a `.env` file with `cp .env.example docker/.env`
4. Create the penpot local network with `docker network create penpot`
5. Start the containers with `docker compose up -d`
6. The Penpot frontend will be available at http://penpot.docker

## TO DO

- [ ] Customise the Penpot image with a `Dockerfile`
- [ ] Adjust the `docker-compose` configuration for a more optimal setup
