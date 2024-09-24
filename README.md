# Simple Symfony Docker Template

A barebones docker-compose setup for Symfony 7, with MySQL, PHP-FPM, and Nginx. **ONLY FOR DEVELOPMENT USE.**

## Prerequisites

Ensure you have the following installed:
- docker
- docker-compose

## Installation
1. **Create a .env file:**
    ```sh
    cp .env.example .env
    ```

2. **Build the Docker containers:**
    ```sh
    docker-compose build
    ```

3. **Start the Docker containers:**
    ```sh
    docker-compose up -d
    ```

4. **Install Composer dependencies:**
    ```sh
    docker-compose exec php composer install
    ```

## Usage

- Visit `http://localhost` in your browser to access the application.

- **Use the following command to enter the PHP container:**
    ```sh
    docker-compose exec php bash
    ```
- **Stop the containers:**
  ```sh
  docker-compose down
  ```
- **View php container logs:**
  ```sh
  docker-compose logs php -f
  ```