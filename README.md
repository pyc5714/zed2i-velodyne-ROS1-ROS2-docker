## reference 
[zed-docker](:https://github.com/stereolabs/zed-docker)
[zed2i docker hub](https://hub.docker.com/r/stereolabs/zed/)
나는 4.0-gl-devel-cuda11.4-ubuntu20.04 를 기반으로 컨테이너 생성

## 1. docker image 
```
docker pull yechanpark5714/zed2i_velodyne_setting_ros1:latest
```

## 2. launch zed2i & velodyne

terminal 1 (velodyne)
```
docker exec -it sensor_setting_ros1 /bin/bash 
source /opt/ros/noetic/setup.bash
source /home/sensor_setting_ros1/devel/setup.bash
roslaunch velodyne_pointcloud VLP16_points.launch
```

terminal 2 (zed2i)
```
docker exec -it sensor_setting_ros1 /bin/bash 
source /opt/ros/noetic/setup.bash
source /home/sensor_setting_ros1/devel/setup.bash
roslaunch zed_wrapper zed2i_amm.launch
```
