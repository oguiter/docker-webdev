# Docker Web Dev
## Description
 - a service for Nginx
 - a service for PHP-FPM
 - a service for MySQL
 - a service for phpMyAdmin
 - a volume to make MySQL data persistent
 - a network for database access
 - a network for HTTP requests

All of the services are using official images.
When building and starting containers for the 
first time with Docker Compose, a database named `project` will be created by default. You can change this in the [`.env`](https://github.com/osteel/docker-tutorial-2/blob/master/.env) file.

A [default Nginx configuration](https://github.com/osteel/docker-tutorial-2/blob/master/nginx/default.conf) is also copied over.

The `www/html/` directory is mounted into the one served by Nginx on the container, so any update to the code is available without having to rebuild the container.

The MySQL data sits in its own directory attached to its own named volume to make it persistent.

The application is available on the port 80 of the host machine.

phpMyAdmin is available on port 8080.
