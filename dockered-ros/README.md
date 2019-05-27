# ROS Docker 

This project will help you to quickly start the development with ROS in Docker container with minimum efforts. Container will open the Gnome Terminator which supports multiple command-line windows and makes it easy to run commands in parallel.

I created this script when I found that official ROS Docker image gives only one command-line prompt per Docker session and no support for GUI applications.

This Docker image is tested on ROS Melodic, Ubuntu Bionic 18.0.4 LTS and Docker 18.09.6

## Requirements

1. Ubuntu
2. Docker. Use the [official installation method](https://docs.docker.com/install/linux/docker-ce/ubuntu). If you download the Docker from Ubuntu Software Center its engine will have no access to X11 sockets and GUI won't start!
3. Docker-compose. [Installation instructions](https://docs.docker.com/compose/install).

## Included Software

1. ROS (current release from [Docker Hub](https://hub.docker.com/_/ros))
2. Gnome Terminator
2. git (latest stable version from [official site](https://git-scm.com/download/linux))
3. Midnight Commander

## Usage

### Building the container

```
cd dockered-ros
docker-compose build --no-cache ros
docker-compose run --name ros_test ros
```

### Starting the container next time

```
docker start ros_test
```

### Using Gnome Terminator

Press Ctrl+Shit+O to open a new terminal splitting the current window horizontally. Ctrl+Shift+E will split the current window vertically.

### Removing all created containers

```
docker-compose rm -f
```