# Image

| Command                                     | Summary                                 |
| :------------------------------------------ | --------------------------------------- |
| `docker pull <image-name>`                  | Pull docker image                       |
| `docker build -f Dockerfile -t <image-name> .` | Create docker image                  |
| `docker images -a`                          | List all images                         |
| `docker login`                              | Login to docker hub                     |
| `docker tag <image-name> username/repo:tag` | Tag <image>                             |
| `docker push username/repo:tag`             | Docker push a tagged image to repo      |
| `docker run username/repo:tag`              | Run image from a given tag              |
| `docker rmi <image-name>`                   | Remove the specified image              |
| `docker rmi $(docker images -q)`            | Remove all docker images                |
| `docker image inspect <image-name>`         | Inspect the given image detail          |

# Container

| Command                                     | Summary                                 |
| :------------------------------------------ | --------------------------------------- |
| `docker run -p 8080:80 <image-name>`        | Start docker container                  |
| `docker run -d -p 8080:80 <image-name>`     | Start docker container in detached mode |
| `docker exec -it <container-name> bash`     | Enter a running container               |
| `docker ps`                                 | List containers                         |
| `docker ps -a`                              | List all containers                     |
| `docker stop <container-name>`              | Stop container                          |
| `docker rm <container-name>`                | Remove container                        |
| `docker rm $(docker ps -a -q)`              | Remove all containers                   |
| `docker kill <container-name>`              | Force shutdown of one given container   |
| `docker logs <container-name>`              | Show the given container logs           |
| `docker inspect <container-name>`           | Inspect the given container detail      |

#  Network

| Command                                     | Summary                                 |
| :------------------------------------------ | --------------------------------------- |
| `docker create network --driver bridge <network-name>`  | Create  bridge network      |
| `docker create network --driver overlay <network-name>` | Create  overlay network     |
| `docker network ls`                         | List networks                           |  
| `docker network inspect <network-name>`     | Inspect given network detail            |

# Compose

| Command                  | Summary                            |
| :----------------------- | ---------------------------------- |
| `docker-compose up`      | Start a compose from yaml file     |
| `docker-compose up -d`   | Start a compose in detached mode   |
| `docker-compose logs`    | Check logs                         |
| `docker-compose down`    | Stop current compose               |
| `docker-compose down -v` | Stop compose and destroy volumes   |

# Docker Machine

| Command                                             | Summary              |
| :-------------------------------------------------  | -------------------  |
| `docker-machine env vm1`                            | Get node env         |
| `docker-machine scp docker-compose.yml vm1:/tmp/`   | Copy files           |
| `docker-machine ssh vm1`                            | ssh to vm            |
| `docker-machine ssh vm1 "docker node inspect <ID>"` | Inspect a node       |
| `docker-machine ssh vm1 "docker node ls"`           | List the nodes       |
| `docker-machine start vm1`                          | Start a VM           |
| `docker-machine stop $(docker-machine ls -q)`       | Stop all running VMs |
| `docker-machine rm $(docker-machine ls -q)`         | Delete all VMs       |

