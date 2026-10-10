# Test Environment

## 1. Project Information

- Project: OWASP Juice Shop — Manual QA Testing
- Document: Test Environment
- Status: Initial baseline
- Verification date: 2026-10-10

## 2. Operating Environment

- Operating System: Linux Mint 22.3
- Architecture: x86_64
- Docker Engine: 29.1.3
- Docker Compose: 2.40.3

## 3. Application Under Test

- Application: OWASP Juice Shop
- Application version: 20.2.0
- Deployment method: Docker
- Container name: juice-shop
- Local URL: http://localhost:3000

## 4. Docker Image

- Image: bkimminich/juice-shop:latest
- Repository digest:
  sha256:73c53fbf442e8337b3ea3d98c7e8550308854701ebdfce4cc39768f36b75430e

The digest identifies the specific image content inspected locally.
The `latest` tag may point to a different image in the future.

## 5. Connectivity Verification

- Verification method: HTTP request using curl
- Request URL: http://localhost:3000
- Observed HTTP status: 200
- Result: Passed

This check confirms that the application responds to an HTTP request.
It does not confirm that all application features work correctly.

## 6. Starting the Application

From the project directory, run:

    cd application/docker
    docker compose up -d

The `-d` option runs the containers in detached mode.

## 7. Stopping the Application

From the `application/docker` directory, run:

    docker compose down

This stops and removes the containers managed by this Compose project.
It does not remove the downloaded Docker image.

## 8. Notes and Limitations

- The Docker image uses the mutable `latest` tag.
- The image digest is recorded to improve reproducibility.
- The HTTP check is a basic connectivity check, not a complete
  functional or security assessment.
- Functional test execution has not yet been documented in this file.
