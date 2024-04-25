# dockerhubimages

1.  Create the image
2.  Publish the image to docker hub
3.  Github actions

#### Imaprtent note

1.  In github need to add the environment variable docker userName and token.
2.  Docker hub token need to generate in docker hub under the myaccount -> security

```bash
# In github/workflow have the all the github action steps like branch, push to docker, docker credentials tags and context
```

## Docker commands

### Local system

```bash
#A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image
docker init

#yml file. It specifies what images are required, what ports they need to expose, whether they have access to the host filesystem, what commands should be run when they start up, and so on
docker compose up --build

#run docker image background
docker compose up --build -d

#stop the docker image
docker compose down

#list of docker images
docker images

#list of running containers
docker ps
```

### Push Docker image to docker hub

```bash
#create repo in hub.docker
1. docker push prashantmalakoti701/api-rate-limit
2. docker login -u prashantmalakoti701
3. docker images
4. docker tag apiratelimit-server(local image name) prashantmalakoti701/api-rate-limit(hub created repo name)
5. docker push prashantmalakoti701/api-rate-limit
```
