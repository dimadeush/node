# Node environment
Docker environment with node 10 for Laravel/Symfony (based on official node docker hub repository).

[Source code](https://github.com/dimadeush/node.git)

## Requirements
* Docker version 18.06 or later
* Docker compose version 1.22 or later

## Integration to your environment
Add next service to your docker-compose.yml:
```
node:
  image: dimadeush/laravel-node
  user: node
  container_name: node
  expose:
    - "8081"
  volumes:
    - ./:/var/www/html
  command: npm run watch
```

## Additional info:
Based on the popular Alpine Linux project. Alpine Linux is much smaller than most distribution base images (~5MB), and thus leads to much slimmer images in general.

## Links
[PHP Laravel environment](https://github.com/dimadeush/docker-apache-php-laravel.git)
[PHP Symfony environment](https://github.com/dimadeush/docker-apache-php-symfony.git)