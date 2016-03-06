Sling docked
============

> Sling application in a docker container


## Install Docker Toolbox

```bash
# Install Homebrew
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# Install Cask
$ brew install caskroom/cask/brew-cask

# Install docker toolbox
$ brew cask install dockertoolbox
```

## Create Docker VM

```bash
# create the docker virtual machine
$ docker-machine create --driver "virtualbox" myBoxName

# start the docker virtual machine
$ docker-machine start myBoxName

# connect docker client to the docker engine running on the virtual machine
$ docker-machine env myBoxName

# configure your shell
$ eval $(docker-machine env myBoxName)
```

## Run the Docker container

```bash
# Build the Dockerfile and tag the image
$ docker build -t sling-docker .

# Run the image inside a container
$ docker run -i -t -p 8080:8080 sling-docker
```



### Reading

- http://stackoverflow.com/a/32770439
- https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices/
