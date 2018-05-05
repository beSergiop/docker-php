# Docker PHP development environment.

[![nginx](https://img.shields.io/badge/nginx-1.13-brightgreen.svg)]()
[![php7.2](https://img.shields.io/badge/php-7.1-brightgreen.svg)]()

These instructions will running on your local machine a dockerized **nginx** + **PHP7.2** environment.

### Prerequisites
As a prerequisite, be sure to [install Docker Compose](https://docs.docker.com/compose/install/) if you have not already done so.

### Initialize environment
We can build the application using `docker-compose up`. This will show the images being built and starting.

```
docker-compose -f docker.dev.yml up
```

### Connect to container environment
The `docker exec` command runs a new command in a running container.
```
docker exec -ti docker_php bash
```

You can access to your test application via [http://localhost:8080](http://localhost/).