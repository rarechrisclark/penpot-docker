# Penpot Docker

This is a Docker Compose configuration for running [Penpot](https://penpot.app) in a self-hosted environment.

Penpot is an open-source design and prototyping platform that is currently in beta. It is a great alternative to Figma, Adobe XD, and other design tools.

Useful reading:
- [Blog | Penpot](https://penpot.app/blog/)
- [Self-hosting Guide | Penpot](https://help.penpot.app/technical-guide/getting-started/#install-with-docker)

## Requirements

- Docker
- Docker Compose
- Nginx-proxy (optional)

## Usage

### First-time setup

- Add `127.0.0.1   penpot.docker` to your `/etc/hosts` file
- Create a `.env` file with `cp .env.example .env` (Note: this will be the default configuration for Penpot)
- Create the `penpot` network with `docker network create penpot`

### Running Penpot

Ensure you have completed the first-time setup before running Penpot.

1. Run `docker-compose up -d` to start the containers
2. Access Penpot on `http://penpot.docker`

Note: When you reach the login page, you can either:
- Create a new account (you will not receive an email... the SMTP configuration is not set up yet. You will get the verification link in the penpot-backend logs)
- Create a demo user

## To-Do

- [ ] Fix the SMTP configuration to send emails
- [ ] Add setup for GitHub OAuth App
- [ ] Configure for use on a subdomain (e.g., `penpot.example.com`)