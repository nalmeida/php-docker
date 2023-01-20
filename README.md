# PHP Docker with Apache

> This project provides a simple way to run PHP applications in a Docker container using Apache as the web server. It includes a pre-configured PHP 8.0.27 environment and Apache.

## Requirements

* `Docker`
* `docker-compose`

### Tested on

* `MacOS 11.5.2`
* `Docker version 20.10.12`
* `docker-compose version 1.29.2`
* `bash-5.2`

## Getting Started

1. Clone the repository to your local machine: git clone https://github.com/nalmeida/php-docker.git
2. Navigate to the project directory: `cd php-docker`
3. Build the Docker image: `docker-compose build`
4. Start the container: `docker-compose up`

Your PHP application should now be running on http://localhost:8080.

## Configuration

You can configure the PHP version and other settings by modifying [docker-compose.yml](./docker-compose.yml) file.

Please note that the `container_name` is not a required field in the compose file and can be removed if not needed.

## Mounting your code

You can mount your code into the container by modifying the [docker-compose.yml](./docker-compose.yml) file and adding a volume under the web service.

Your code is located in the `src` directory of your project, you can add the following line under the web service:

```
volumes:
  - ./src:/var/www/html
```

## Stopping the container

To stop the container, you can use the command `docker-compose down` or `CTRL+C` on your terminal.

## Support

If you have any issues or questions, please open an issue in the GitHub repository.

## Links

Based on the post: https://www.section.io/engineering-education/dockerized-php-apache-and-mysql-container-development-environment/