# Docker
- https://www.youtube.com/watch?v=gAkwW2tuIqE
- https://www.youtube.com/watch?v=3c-iBn73dDE&t=250s
![image](https://user-images.githubusercontent.com/11143215/165758800-c1f9fbba-4b26-495d-bce7-5b0679751fe9.png)

# Containers
- https://www.youtube.com/watch?v=pTFZFxd4hOI&t=430s
![image](https://user-images.githubusercontent.com/11143215/165864021-53f79534-5504-4e64-b21e-aeb17db70e81.png)

## Build YOUR OWN Dockerfile, Image, and Container
- https://www.youtube.com/watch?v=SnSH8Ht3MIc&list=WL&index=5

# Image
### Image consists of the following 
![image](https://user-images.githubusercontent.com/11143215/165864441-0599406e-2194-4b75-ac02-108e0e61585b.png)

``` The docker image is readonly and cannot be changed once created. If we do some changes in the codebase then we build another image. This is where we utilize the tag. We can version our image ```

# Dockerfile
https://takacsmark.com/dockerfile-tutorial-by-example-dockerfile-best-practices-2018/
We can take any application and dockerize it by adding Dockerfile into it
- Docker file consists of instructions for packaging an application into an image. Once we have the Docker image we can run it anywhere. Any machine where the   docker engine is installed.

![image](https://user-images.githubusercontent.com/11143215/165869251-22c3e69b-f001-480b-b504-c9db029172a9.png)

## Dockerize .NET 6 in 10 Minutes
- https://www.youtube.com/watch?v=3s-RfwvijpY&t=555s
![Screen Shot 2022-07-07 at 1 21 34 pm](https://user-images.githubusercontent.com/11143215/177683760-cc2bea93-5288-4f7a-8d56-a5f118c6f555.png)


# Docker Commands
https://docs.docker.com/engine/reference/commandline/docker/
https://dockerlabs.collabnix.com/docker/cheatsheet/
https://www.edureka.co/blog/docker-commands/
- ``` docker --version ``` => get the currently installed version of docker
- ``` docker build . ``` => docker run build and look for the dockerfile in relative path . (. the current folder)
- ``` docker build -t name-u-want-to-for-image:tag-that-u-wantto-give . ``` => Builds the image with the name and tag that u wanted, the period (.)
is the path to the Dockerfile. In this example it is the current directory
- ``` docker ps ``` => list of processes or running containers
- ``` docker ps -a ``` => List of all the containers
- ``` docker exec -it <container id> bash ``` => access the running container
- ``` docker run -it -d <image name> ``` => create a container from an image
- ``` docker pull <image name> ``` => pull images from the docker repository(hub.docker.com)
- ``` docker stop <container id> ``` => stops a running container
- ``` docker kill <container id> ``` => This command kills the container by stopping its execution immediately. The difference between ‘docker kill’ and ‘docker stop’ is that ‘docker stop’ gives the container time to shutdown gracefully, in situations when it is taking too much time for getting the container to stop, one can opt to kill it
- ``` docker commit <conatainer id> <username/imagename> ``` => creates a new image of an edited container on the local system
- ``` docker login ``` => used to login to the docker hub repository
- ``` docker push <username/image name> ``` => used to push an image to the docker hub repository
- ``` docker images ``` => lists all the locally stored docker images
- ``` docker rm <container id> ``` => used to delete a stopped container
- ``` docker rmi <image-id> ``` => used to delete an image from local storage
- ``` docker build <path to docker file> ``` =>  build an image from a specified docker file

## Docker run explained
``` docker run -d --name name-0f-container -p 8080:80 name-of-the-image-to-use ```
#### -d = run the container in detached mode (in the background)
#### --name = the name that you want to give to the container
#### -p = map the port from the container to your machine. the left side is your machine's port. The port that you want to be in your machine. The right hand side will be port number of your docker container. (8080:80 => left side is your machine and right side is the image)


## Open the container in the interactive(it) mode
``` docker run -it <container_name> ```

### Interact with the ubuntu shell using docker
``` docker run ubuntu ```
    - This will pull the latest ubuntu image from the registry and start the container if the image is not available locally
    - Alternatively we can use ```docker pull ubuntu ```
#### Now start playing around with the linux command in the cell

## Simple steps to try nginx/docker
        FROM nginx:1.10.1-alpine
        COPY src/html usr/share/nginx/html
        # Copy our html files from src/html location to the nginx's usr/share/nginx/html where it keeps the files 
        # EXPOSE 80
        # CMD [ "nginx", "-g","daemon off;"  ]
        #This cmd command is ran by nginx in default so we can leave this one if we are not making any changes
        # AN IMAGE BECOMES A CONTAINER WHEN WE EXECUTE IT
### Start Building the image and spinning the container => example -> follow the steps
        docker build -t hello-internet:mytag .
        docker run -d --name myContainerName -p 80:80 hello-internet:mytag  
        
        
        
