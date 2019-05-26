# Repository for ROS Projects

## Building the container

```
cd dockered-ros
docker-compose build --no-cache ros
docker-compose run --name ros_test ros
```

## Starting the container next time

```
docker start ros_test
```

## Removing all created containers

```
docker-compose rm -f
```
