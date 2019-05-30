# Dockered ROS 

This project will help you to quickly start the development with ROS in Docker container with minimum efforts. Container will open the Gnome Terminator which supports multiple command-line windows and makes it easy to run commands in parallel.

I created this script when I found that official ROS Docker image gives only one command-line prompt per Docker session and no support for GUI applications.

This Docker image is tested on ROS Melodic, Ubuntu Bionic 18.0.4 LTS and Docker 18.09.6

## Requirements

1. Ubuntu
2. Docker. Use the [official installation method](https://docs.docker.com/install/linux/docker-ce/ubuntu). If you download the Docker from Ubuntu Software Center its engine will have no access to X11 sockets and GUI won't start!
3. Docker-compose: [installation instructions](https://docs.docker.com/compose/install).

## Included Software

1. ROS (current release from [Docker Hub](https://hub.docker.com/_/ros))
2. Gnome Terminator
2. git (latest stable version from [official site](https://git-scm.com/download/linux))
3. Midnight Commander

## Usage

### Building the container

```
cd ~
git clone https://github.com/MaxZhaloba/ros.git
cd ros/dockered-ros
xhost +local:docker
docker-compose build --no-cache ros
docker-compose run --name ros_test ros
```

### Starting the container next time

```
xhost +local:docker
docker start ros_test
```

### Using Gnome Terminator

| Hotkey | Action |
| Ctrl+Shit+O | Open a new terminal splitting the current window horizontally |
| Ctrl+Shift+E | Split the current window vertically |
| Ctrl+Shift+I | Open a new window |

### Removing all created containers

```
docker-compose rm -f
```