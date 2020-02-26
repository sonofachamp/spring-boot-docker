# Example Dockerized Spring Boot Application

## Build

`./mvnw package`

## Run locally

`./mvnw spring-boot:run`

## Docker

`docker build -t spring-boot-docker .`

`docker run -p 8080:8080 -p 8081:8081 spring-boot-docker`

`curl localhost:8080`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hello, Spring!</title>
</head>
<body>
    Hello, Spring!
</body>
</html>
```

`curl -s localhost:8081/actuator/health | jq`

```json
{
  "status": "UP"
}
```
