# Symfony Base Repository

This repository contains the basic configuration to run Symfony applications with MySQL database

## Content
- PHP-APACHE container running version 8.2
- MySQL container running version 8.2.0

## Instructions
- `make build` to build the containers
- `make start` to start the containers
- `make stop` to stop the containers
- `make restart` to restart the containers
- `make prepare` to install dependencies with composer (once the project has been created)
- `make logs` to see application logs
- `make ssh` to SSH into the application container

## Create and Run the application
- [Optional] Replace all the occurrences of symfony-app in the whole project with some name more meaningful for your project
- `make start` to build and start the containers (you can use your IDE find and replace option to do so)
- SSH into the container with `make ssh`
- Create a Symfony project using the CLI (e.g. `symfony new --no-git --dir project`). See `symfony`command info for more options
- Move all the content in the `project` folder to the root of the repository (do not forget to move also `.env`file)
- Add the content of `.gitignore` file to the root one, it should look like this
```
.idea
.vscode
docker-compose.yml

###> symfony/framework-bundle ###
/.env.local
/.env.local.php
/.env.*.local
/config/secrets/prod/prod.decrypt.private.php
/public/bundles/
/var/
/vendor/
###< symfony/framework-bundle ###
```
- Once you have installed you Symfony application go to http://localhost:1000
