# Working ROS image

This is a docker image with additional configuration which I use for development.

Building

```
xhost +local:docker
docker-compose build --no-cache my_ros
docker-compose run --name my_ros_test my_ros
```

Starting again

```
xhost +local:docker
docker start my_ros_test
```