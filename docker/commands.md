# Here commands cover the main Docker functionalities for creating, 
# managing, and troubleshooting containers and images


docker ps
# Role: Lists all currently running containers.
# Usage: Shows essential details like container ID, name, status, and ports.

docker ps -a
# Role: Lists all containers, including stopped ones.
# Usage: Useful for reviewing past containers or checking the status/history of containers.

docker logs -f <container>
# Role: Follows and displays real-time logs for a specific container.
# Usage: Helps monitor a container’s output or troubleshoot errors.

docker exec -it <container> <command>
# Role: Runs a command inside a running container with interactive access (-it flag).
# Usage: Often used to open a shell session (bash or sh) within the container.

docker run -d -p <vm_port>:<container_port> --name=<container_name> <image>
# Role: Creates and starts a container in detached mode (-d), exposing it on a specified port.
# Usage: Essential for running apps or services and making them accessible through the VM.

docker build -t <tag_name> .
# Role: Builds a Docker image from a Dockerfile in the current directory, assigning a tag.
# Usage: Used to create a custom image with specified configurations.

docker container inspect <container>
# Role: Provides detailed information about a container, such as its environment, volumes, network settings, and more.
# Usage: Helpful for troubleshooting and checking container properties.

docker images
# Role: Lists all Docker images on the system.
# Usage: Useful for reviewing available images before creating containers.

docker rm <container>
# Role: Deletes a container by ID or name.
# Usage: Cleans up unused containers, freeing system resources.

docker rmi <image>
# Role: Removes an image from the local Docker registry.
# Usage: Helps manage disk space by deleting unused or outdated images.

docker stop <container>
# Role: Gracefully stops a running container.
# Usage: Useful for controlled shutdowns without immediate termination.

docker kill <container>
# Role: Immediately stops a container by sending a SIGKILL signal.
# Usage: Forcibly terminates a container, useful for emergencies.

docker volume ls
# Role: Lists all Docker volumes on the system.
# Usage: Essential for managing and cleaning up storage volumes.

docker network ls
# Role: Displays all Docker networks on the system.
# Usage: Useful to review network configurations and isolate services.

docker pull <image> 
# Role: Downloads an image from Docker Hub or a registry.
# Usage: Fetches a specific image version for local use.

docker push <image> 
# Role: Uploads an image to Docker Hub or a registry.
# Usage: Shares your custom images publicly or privately.

docker tag <image> <new_image:tag> 
# Role: Renames or tags an image with a new name or version.
# Usage: Prepares an image for versioning or publishing.

docker stop <container> 
# Role: Gracefully stops a running container.
# Usage: Stops the specified container by sending a termination signal.

docker start <container> 
# Role: Starts a previously stopped container.
# Usage: Restarts an existing container without creating a new one.

docker restart <container> 
# Role: Restarts a running or stopped container.
# Usage: Stops, then immediately starts a specified container.

