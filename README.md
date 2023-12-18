# Symfony Base Repository

This repository contains the basic configuration to run Symfony applications with MySQL database

## Content
- PHP-APACHE container running version 8.2
- MySQL container running version 8.2.0

## Instructions
- **[optional]** Replace all the occurrences of **symfony-app** in **docker-compose.yml.dist** and **Makefile** with some name more meaningful for your project
- `make build` to build the containers
- `make start` to start the containers
- `make stop` to stop the containers
- `make restart` to restart the containers
- `make prepare` to install dependencies with composer (once the project has been created)
- `make logs` to see application logs
- `make ssh-be` to SSH into the application container

## Running the application
Once you have installed you Symfony application go to http://localhost:1000
