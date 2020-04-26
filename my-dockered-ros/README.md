# Working ROS image

This is a docker image with additional configuration which I use for development.

Building

Build the [../dockered-ros](../dockered-ros) project at first

```
xhost +local:docker
docker-compose build --no-cache ros
docker-compose run --name my-ros-test ros
```

Starting again

```
xhost +local:docker
docker start my_ros_test
```