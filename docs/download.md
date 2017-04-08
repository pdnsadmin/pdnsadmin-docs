### Getting pdnsAdmin

#### Normal release

The most recent version is pdnsAdmin 1.0.1, which was released on Jan 2rd, 2017. 

There are *two ways* getting pdnsAdmin up and running on your own system:

#### 1. Get Full Source code
It can be got the latest full source code at:

    git clone git://github.com/pdnsadmin/pdnsadmin.git
    or 
    git clone https://github.com/pdnsadmin/pdnsadmin.git

GitHub creates automatically a tarball of the latest revision of the regular pdnsAdmin code and it can been downloaded from:

    https://github.com/pdnsadmin/pdnsadmin/zipball/master

#### 2. Docker images
For your convinience, pdnsAdmin is also supported docker image which you you bring it up on you system within few minutes.

    docker pull pdnsadmin/pdnsadmin:latest

Pull latest docker images and get it running

Please read [Setup](http://doc.pdnsadmin.com/setup) to have the detail how to setup pdnsAdmin with Docker.

#### Supported Docker versions
This image is officially supported on Docker version 1.12.5.

Support for older versions (down to 1.6) is provided on a best-effort basis.

Please see [the Docker installation documentation](https://docs.docker.com/installation/) for details on how to upgrade your Docker daemon.
