## Running with Docker

This project provides Docker support for building and running the Spring Boot Config Server using Java 17 (Eclipse Temurin). The application is exposed on port `8080`.

### Requirements
- Docker (with Compose)
- No external services or persistent volumes required
- Java 17 (Eclipse Temurin) is used in both build and runtime stages

### Build and Run

To build and start the service:

```sh
# Build and start the config server
docker compose up --build
```

This will build the image using the provided Dockerfile and start the service as `java-config_server`.

### Ports
- The service is available on `localhost:8080` (mapped from the container)

### Environment Variables
- No required environment variables are set by default
- If you need to provide custom environment variables, you can create a `.env` file and uncomment the `env_file` line in `docker-compose.yml`

### Additional Notes
- The container runs as a non-root user for security
- No additional configuration is required for basic usage
- If you add external services (e.g., databases), update `docker-compose.yml` accordingly

For more details, see the provided `Dockerfile` and `docker-compose.yml`.