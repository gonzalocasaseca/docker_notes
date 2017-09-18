#Containers

##Attach a running container
We can attach with the name or the id

~~~bash
docker attach jolly_lovelace
~~~


#Check differences

~~~bash
docker diff 6d1020d669ab
~~~

#Stop container

~~~bash
docker stop 6d1020d669ab
~~~

#See running containers

~~~bash
docker ps
~~~

#See all containers in any state

~~~bash
docker ps -a
~~~

#Start stopped container

~~~bash
docker start 6d1020d669ab
~~~

#Start and attach stopped container

~~~bash
docker start -a 220637a2b8fa
~~~

#Restart container

~~~bash
docker restart 220637a2b8fa
~~~


#Pause & unpause

~~~bash
docker pause/unpause 220637a2b8fa
~~~

##Remove container

~~~bash
docker rm 7473f2568add
~~~

Remove all the non running ones

~~~bash
docker rm $(sudo docker ps -aq -f state=exited)
~~~

Or

~~~bash
docker container prune
~~~

##Commit the changes

~~~bash
docker commit 220637a2b8fa
~~~

To add a name

~~~bash
docker commit 220637a2b8fa learningdocker/ubuntu_wget
~~~

Add commit from container name and a comment

~~~bash
docker commit -m="NewImage for second edition" containerforhub  vinoddandy/imageforhub2
~~~

##Show container logs
docker logs 32986a76d619