## Docker up and running
pdnsAdmin App container and MySQL container

pdnsAdmin docker image has been built with latest source code and ready for up and running.

*Setup pdnsAdmin docker*

    docker pull pdnsadmin/pdnsadmin 

It will pull latest pdnsAdmin docker image which contains latest pdnsAdmin source code.
Or you can select tag name to pull the specify pdnsAdmin version.

*Example*: we'd like to pull specify version `v1.0.1`
    docker pull `pdnadmin/pdnsadmin:v1.0.1`

#### How to use docker image

Start a pdnsAdmin server instance
Starting a pdnsAdmin instance is simple:

    $ docker run --name=pdnsadmin-name -d pdnsadmin:tag

where pdnsadmin-name is the name you want to assign to your container, tag is the tag specifying the pdnsAdmin version you want. See the list above for relevant tags.

Get IP docker container pdnsAdmin running

    $ docker inspect --format '{{ .NetworkSettings.IPAddress }}' pdnsadmin-name

You can hit `$curl http://<docker-container-ip>:80` in your command line interface.

in case, you would like to expose the nginx port of pdnsadmin container to host, please add -p option in docker run command

    $ docker run --name=pdnsadmin-name -d -p 8080:80 pdnsadmin:tag

Then you can hit `http://localhost:8080` or `http://host-ip:8080` in your browser. (if you expose `8080` port to host)

*Note*: This step, You would have pdnsAdmin ready and running and require to have MySQL server and PowerDNS ready to connect.
pdnsAdmin will need some more basic steps to set it up like connect to Database and PowerDNS API.

# Quick start: Docker Composer

With docker composer supports, you can get pdnsAdmin up and running by single command.

Check out this git repo and its document

    $ git clone https://github.com/pdnsadmin/pdnsadmin-docker-compose

Build and start services

    docker-compose build
    docker-compose up

*Detail:* [https://github.com/pdnsadmin/pdnsadmin-docker-compose/blob/master/README.md](https://github.com/pdnsadmin/pdnsadmin-docker-compose/blob/master/README.md)