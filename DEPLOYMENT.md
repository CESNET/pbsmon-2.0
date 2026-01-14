# Deployment Guide

## Purpose

This document provides instructions for deploying the PBSMon web application.

## Prerequisites

- Docker
- Kerberos
- Running on Debian 13

## Configuration

- set <rootDir>/.env
- run

```sh
cp .env.prod.example .env
```

**⚠️ Security Warning**: These mock data files contain sensitive information and must be transferred through a **secure channel** . Do not commit sensitive mock data to version control.

## Deploying

to deploy:

```sh
./deploy.sh
```

In case of need to restart nginx, run

```sh
sudo docker compose -f docker-compose.prod.yml restart -d nginx
```

TODO:

- make deploy.sh great again - it needs to work
- add configuration for nginx to .env, dont hardcode it
- how to make a new PBS machines works and to be configured
