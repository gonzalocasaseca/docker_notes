#Docker Images
##Pull image
~~~bash
docker pull hello-world
~~~

```<repository>:<tag>``` to pull an specific version:

~~~bash
docker pull busybox:1.24
~~~

###Pull third party image
~~~bash
docker pull thedockerbook/helloworld
~~~

###Pull third party hub or local
~~~bash
docker pull registry.example.com/myapp
~~~


##Push Image

~~~bash
docker push vinoddandy/imageforhub2 
~~~

##List downloaded images
~~~bash
docker images
~~~

By default, the docker images subcommand will only show 12 hex digits. You can display all the 64 hex digits using the ```--no-trunc```

##Run image
~~~bash
docker run hello-world
~~~

###Launch an interactive container
~~~bash
docker run -i -t ubuntu:16.04 /bin/bash
~~~

###Run interactive container and remove it once is fishined
~~~bash
docker run -i -t --rm ubuntu:16.04 /bin/bash
~~~

###Run and set a container name
~~~bash
docker run -i --name="containerforhub" -t ubuntu /bin/bash
~~~
 
###Run as daemon
~~~bash
docker run -d ubuntu
~~~

##Search for image
~~~bash
docker search mysql
~~~

##Tag image
~~~bash
docker tag 0a2abe57c325 busyboxplus
~~~


##See the image layers
~~~bash
docker history <image_id/image_name>
~~~

