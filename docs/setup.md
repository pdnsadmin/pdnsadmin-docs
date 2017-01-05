## Docker setup have two parts
pdnsAdmin App container and MySQL container

pdnsAdmin docker image has been built with latest source code and ready for up and running.

1. Setup pdnsAdmin docker

    docker pull pdnsadmin 

It will pull latest pdnsAdmin docker image which contains latest pdnsAdmin source code.
Or you can select tag name to pull the specify pdnsAdmin version.

Example we'd like to pull specify version v1.0.1
    docker pull pdnsadmin:v1.0.1

#### How to use this image

Start a pdnsAdmin server instance
Starting a pdnsAdmin instance is simple:

$ docker run --name=pdnsadmin-name -d pdnsadmin:tag
... where pdnsadmin-name is the name you want to assign to your container, tag is the tag specifying the pdnsAdmin version you want. See the list above for relevant tags.

Get IP docker container pdnsAdmin running
    $ docker inspect --format '{{ .NetworkSettings.IPAddress }}' pdnsadmin-name
You can hit $curl http://<docker-container-ip>:80 in your command line interface.

in case, you would like to expose the nginx port of pdnsadmin container to host, please add -p option in docker run command

$ docker run --name=pdnsadmin-name -d -p 8080:80 pdnsadmin:tag

Then you can hit http://localhost:8080 or http://host-ip:8080 in your browser. (if you expose 8080 port to host)

Note: Dockerfile is located at 

###### Exposing the port for docker container

    $ docker run --name pdnsadmin -d -p 8080:80 pdnsadmin

Then you can hit http://localhost:8080 or http://host-ip:8080 in your browser.
