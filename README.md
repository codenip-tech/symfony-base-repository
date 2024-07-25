# Symfony Base Repository

This repository contains the basic configuration to run Symfony applications with MySQL database

## Content
- PHP-APACHE container running version 8.3
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
> [!TIP]
> Replace all the occurrences of `symfony-app` in the project with a more meaningful name. 
> You can use your IDE's find and replace option to complete this task.

> [!TIP]
> Select your Symfony `version` updating the URL.

1. Build and start the containers:
    ```shell
    make start
    ```
2. SSH into the container:
    ```shell
    make ssh
     ```
3. Download the composer.json from [Symfony Skeleton](https://github.com/symfony/skeleton):

    <details open>
    <summary>Version 6.4 (LTS)</summary>

   ```shell
    wget https://raw.githubusercontent.com/symfony/skeleton/6.4/composer.json
    ```
    </details>
    <details>
    <summary>Version 7.1</summary>

   ```shell
    wget https://raw.githubusercontent.com/symfony/skeleton/7.1/composer.json
    ```
    </details>
4. Install with composer

   ```shell
    composer install --no-interaction
    ```
5. Once you have installed you Symfony application go to http://localhost:1000
