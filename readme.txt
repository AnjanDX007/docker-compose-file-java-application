In this file, we define two services: db and app. The db service is based on the MySQL 8.0 image and uses environment variables to set the root password, 
database name, user, and password. The app service is based on the OpenJDK 11 JDK slim image and mounts the current directory as a volume at /app. 
It runs the ./mvnw spring-boot:run command, which is used to start the Spring Boot application. Finally, it maps port 8080 on the host to port 8080 in the container and depends on the db service,
meaning that the db service must be started before the app service.

To start the services, run the following command in the same directory as the docker-compose.yml file:

docker-compose up