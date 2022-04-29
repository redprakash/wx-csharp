# Docker
- https://www.youtube.com/watch?v=3c-iBn73dDE&t=250s
![image](https://user-images.githubusercontent.com/11143215/165758800-c1f9fbba-4b26-495d-bce7-5b0679751fe9.png)

# Containers
- https://www.youtube.com/watch?v=pTFZFxd4hOI&t=430s
![image](https://user-images.githubusercontent.com/11143215/165864021-53f79534-5504-4e64-b21e-aeb17db70e81.png)

# Image
### Image consists of the following 
![image](https://user-images.githubusercontent.com/11143215/165864441-0599406e-2194-4b75-ac02-108e0e61585b.png)

# Dockerfile
We can take any application and dockerize it by adding Dockerfile into it
- Docker file consists of instructions for packaging an application into an image. Once we have the Docker image we can run it anywhere. Any machine where the   docker engine is installed. 

# Docker Commands
#### docker ps => list of processes or running containers
#### docker ps -a => List of all the containers

### Open the container in the interactive(it) mode
``` docker run -it mycontainer ```

### Interact with the ubuntu shell using docker
``` docker run ubuntu ```
    - This will pull the latest ubuntu image from the registry and start the container if the image is not available locally
    - Alternatively we can use ```docker pull ubuntu ```
### start playing around with the linux command in the cell
