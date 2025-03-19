# DevOps Portfolio - Docker Containerization & Deployment

This repository demonstrates my experience in containerizing an existing Python application and deploying it to Docker Hub. The goal of this project was to modernize the application using Docker, making it more scalable, portable, and easier to manage in different environments.

## Overview

The task was to containerize a Python-based distance conversion application and publish the Docker image to Docker Hub. By doing so, I showcased my skills in **Docker**, **containerization**, and **cloud deployment**.

### Key Activities:
- **Containerization of the Application**: I created a `Dockerfile` to containerize the existing Python application, ensuring it could run consistently across different environments.
- **Building the Docker Image**: I built the Docker image and ran tests to ensure it was functioning properly within the container.
- **Publishing to Docker Hub**: Once the image was tested and verified, I published it to **Docker Hub**, making it publicly available for others to pull and use.
- **Documentation**: I documented the process of building, testing, and deploying the Docker container to Docker Hub, making it easy for anyone to replicate or contribute to the project.

## Steps Followed:

### 1. Dockerfile Creation

To containerize the existing application, I created a `Dockerfile` with the following key instructions:

- **Base Image**: Used the official `python:3.9-slim` image to keep the container lightweight.
- **Dependencies**: Installed the necessary Python dependencies from `requirements.txt`.
- **Exposing Ports**: Exposed port 5000 to allow external access to the Flask application running inside the container.
- **Run Flask Application**: Configured the container to run the Flask app using `flask run --host=0.0.0.0`, enabling external connections.

### 2. Building the Docker Image
I built the Docker image using the following command:

```bash
docker build -t conversao-distancia .
```

This command created a Docker image tagged `conversao-distancia`, which could be used to create containers based on this image.

### 3. Running the Container Locally
After building the image, I ran the container locally using the following command:

```bash
docker run -p 5000:5000 conversao-distancia
```

This mapped port 5000 of the container to port 5000 on the host machine, making the application accessible at http://localhost:5000.

### 4. Publishing the Image to Docker Hub
After verifying that the application was working correctly in the Docker container, I published the image to Docker Hub for easy access and distribution.

#### Tagging the Image:

```bash
docker tag conversao-distancia your-username/conversao-distancia:latest
```

#### Pushing to Docker Hub:

```bash
docker push your-username/conversao-distancia
```

**Result**: The image was successfully pushed to Docker Hub and can now be pulled by anyone with the link.

### 5. Documentation (dockerhub.md)
As part of the project, I also created a `dockerhub.md` file in the repository, which documents the Docker Hub image and provides a link to it for easy access by other developers.

```markdown
# DockerHub - Application Image

The container image has been published to DockerHub and can be accessed through the following link:

🔗 [DockerHub Image Link](https://hub.docker.com/r/your-username/conversao-distancia)
```

## Conclusion
Through this project, I demonstrated key DevOps skills related to Docker, including containerization, image building, and publishing to Docker Hub. This process not only modernized the application but also made it more portable and scalable, which is a key objective in today's cloud-based infrastructure.

The project also highlights my ability to collaborate with developers and take an existing application and make it ready for containerized deployment, ensuring it can be easily managed in various environments, from local to cloud platforms.

