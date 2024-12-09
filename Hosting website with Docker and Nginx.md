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

- Use the following command to reveal if the docker has exited:

```
docker ps -a
```

- Use the following command to check the container's ID:

```
docker run --name docker-nginx -p 80:80 -d nginx
```

- Use the following command to get new information about container:

```
docker ps
```

- Use the following command to stop the container:

```
docker stop docker-nginx
```

- Remove the default Nginx page and create new custom html file using following commands:

```
docker rm docker-nginx
```
```
mkdir -p ~/docker-nginx/html
```

- Navigate to the file created:

```
cd ~/docker-nginx/html
```

- Now, create an ''index.html'' and write an HTML code on ''vim'' code editor:

```
vi index.html
```

- Write the code and save the file, then connect the file to the instance:

```
docker run --name docker-nginx -p 80:80 -d -v ~/docker-nginx/html:/user/share/nginx/html nginx
```

### Now check the linksting-website-using-Docker-and Nginx.md
