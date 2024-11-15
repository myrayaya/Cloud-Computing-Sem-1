## Hosting a website with Docker and Nginx

Step - 1: Login to your AWS Account and launch the EC2 Instance

Step - 2: Launch PuTTY and add the IP Address from the Instance and add the key pair file and open the PuTTY Terminal

Step - 3: Login to the OS by writing `ubuntu`

## Installation of Docker

```
curl -sL https://github.com/ShubhamTatvamasi/docker-install/raw/master/docker-install.sh | bash
```

- Type the following command to avoid using `sudo` 

```
newgrp docker
```

- Then type this (It will provide a list of the Docker Containers on your machine)

```
docker ps
```

- You can check your docker version by typing:

```
docker --version
```

- To use `Nginx` in our container, use the following commands:

```
docker pull nginx
```

```
docker run --name docker-nginx -p 80:80 nginx
```

## Using the Instance's IP and view Nginx default webpage

- Use the following command to stop the container from running:

```
docker stop <container id>
```

- Use the following command to reveal if the docker 
