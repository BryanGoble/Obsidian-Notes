---
tags:
  - Linux
  - Docker
---

# Linux Services
- `systemctl <status|start|stop> docker` - control docker daemon from terminal
- `dockerd` - used to control docker daemon if systemctl is crashing or causing issues. **Requires admin privileges | sudo**
- `dockerd --debug` - run dockerd in debug mode if tracking errors
# Docker command essentials
- `docker pull <container-name>` - downloads latest container image, but does not run it.
- `docker pull <container-name>:version` - specify the desired version of the image that you want to download. You can also use `:lts` to grab the latest long-term support image
- `docker run <container-name>` - downloads latest container image (starting with local then remote) and starts the container. Container will run with default commands.
- `docker run --name=<custom-name> <container-name>` - allows you to specify a custom name space for your container
- `docker run --network=<network-name> <container-name>` - specify default or custom network names
- `docker run -it <container-name>` - Does the same as above, but runs the container in interactive mode with teletype (allows console/terminal input) waiting for user input rather than running default commands.
- `docker run -d -p <host-port>:<service-port> <container-name>` - downloads and runs the container in detached mode on the specified service port. Allowing us to connect to the container via the host port. Example: `docker run -d -p 80:8080 jenkins/jenkins` verify the connection in the browser with `localhost:8080`.
- `docker exec <container-name> <commands>` - runs the container and executes specified commands.
- `docker container ls` or `docker ps` - lists all currently active (up) containers
- `docker container ls -a` or `docker ps -a` - lists all containers that are active or previously active
- `docker <start|stop> <container-id or container-name>` - manually start/stop container
- `docker inspect <container-name or container-id>` - view the image or container configuration json
- `docker rm <container-id or container-name>` - removes container, but not the image
- `docker container prune` - removes all inactive containers, freeing up space
- `docker images` or `docker image ls` - view downloaded images on machine
- `docker rmi <container-id or container-name>` or `docker image rm <container-id or container-name>` - removes specified image from disk
- `docker network ls` - view available networks and their types
- `docker network inspect <network-id>` - view more information about specified network
- `docker rm $(docker ps -aq)` - uses the `docker ps` command as a variable listing all container ids then removing them.

# Docker Networks
- 3 Types:
	1. Bridge Network
		- Default network for most containers or if network isn't specified during container install
		- `docker run <container-name>`
		- Container obtains IP dynamically from within the same subnet as the Docker host
	2. None Network
		- No network connection at all
		- Use this type for containers that should remain isolated, such as, when performing malware analysis
		- `docker run <container-name> --network=none`
	3. Host Network
		- Container runs on same IP as the host, but tied to a specific port. Ports cannot be shared between containers.
		- `docker run <container-name> --network=host`
- When Docker is first installed a default Bridge network is initially setup.
	- To view this network, use `ip link`. This shows the available networks on the physical host including the docker bridge.
	- You can use `inspect` to view a containers particular network setup as well.
- `docker network create --driver=bridge --subnet=<custom-ip>/<subnet-mask> <custom-network-name>` - This command is used to create custom bridged subnets that specific containers can connect to while still being isolated from all others.
- `docker network connect <network-name> <container-id>` - manually connect container to network after creation
- `docker network disconnect <network-name> <container-id>` - manually disconnects container from specified network
- `docker network rm <network-id>` - remove available network from docker
- `docker network prune` - removes all custom networks

# Volumes
- Containers normally save all of their data to their own read/write layer that is also deleted once the container is removed. If you want the data to persist after container deletion then we can use volumes that are external to the container to save all data instead.
- `docker volume create <custom-volume-name>` - initialize a custom volume that can be used to store container data once assigned
- `docker run -itd -v <custom-volume-name>:/<folder-name> <container-name>` - docker will create the container and assign the folder-name as the storage location for all data that is saved to the custom volume.
	- You can either use local folder locations on the docker host as a custom volume or use the `volume create` command above to then specify the volume name. This creates a bind mount rather than volume mount.
- `docker volume ls` - list all available volumes stored in the default docker volumes directory (`/var/lib/docker/volumes`)
- `docker run -itd --mount type=bind,source=<local-directory>,target=/<folder-name> <container-name>` - alternative method of creating mounts with containers.
- `docker volume rm <volume-name>` - deletes the specified volume