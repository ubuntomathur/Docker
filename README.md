# Docker #
Docker_DataBase_Dreams

![Image Alt](https://github.com/ubuntomathur/Docker/blob/main/2025-04-05_23-24-44.jpg)


🔹 1. Client
The user interacts with Docker through the client using commands like:

docker build – builds an image from a Dockerfile.

docker pull – downloads an image from a remote registry (like Docker Hub).

docker run – creates and starts a container from an image.

🔹 2. Docker Host
This is the system (physical or virtual machine) where Docker is installed.

Contains the Docker Daemon (dockerd) that listens for commands from the client and manages:

Containers – running instances of Docker images.

Images – templates used to create containers (e.g., Ubuntu, Redis, etc.).

🧠 What happens inside:
The Docker daemon:

Pulls images from the Registry when needed.

Stores images locally.

Uses those images to create containers.

Builds new images from a Dockerfile if docker build is used.

🔹 3. Registry
A repository for Docker images (e.g., Docker Hub, Harbor, Nexus).

Stores public or private images like:

Ubuntu

Redis

NGINX

CentOS (icon in the diagram)

🔄 Image Flow:
When the client runs docker pull, the daemon downloads the image from the registry to the host.

When docker run is used, it checks if the image is available locally; if not, it pulls it from the registry.

docker build can optionally push a new image to the registry using docker push.

🔁 Arrows Summary:
Dashed arrows represent control or command flows.

Solid arrows show data flow:

From registry to host (image pull),

From image to container (container creation),

From client to Docker daemon (command trigger).

🧩 Key Concepts Shown:
Docker images are immutable templates stored in the registry or locally.

Containers are the runnable instances of those images.

The Docker daemon is the brain that manages all Docker operations.


A Docker image is immutable, meaning:

Once the image is created, you can't change it directly.
