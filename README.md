# pcl_ros_processing
pcl sample program on ROS(Robot Operating System)

# usage
Please prepare rgbd sensor(ex:Kinect, Realsense) and build this package

## downsampling
```sh
$ rosrun pcl_ros_processing downmpling input:=/SR300/depth/points
```

## planar segmentation
```sh
$ rosrun pcl_ros_processing planar_segmentation input:=/camera/depth_registered/points
```

for rviz visualization
```sh
$ rosrun rviz rviz
```

```sh
$ pcl_viewer save.pcd
```
press `5` for color visualization

## color filter
for rgb
```sh
$ rosrun pcl_ros_processing color_filter_rgb input:=/camera/depth_registered/points
```

for hsv

```sh
$ rosrun pcl_ros_processing color_filter_hsv input:=/camera/depth_registered/points
```

for rviz visualization
```sh
$ rosrun rviz rviz
```

```sh
$ pcl_viewer save.pcd
```
press `5` for color visualization


# References

## planar segmentation
- http://wiki.ros.org/pcl/Overview
- http://pointclouds.org/documentation/tutorials/planar_segmentation.php#planar-segmentation
- https://staff.aist.go.jp/kanezaki.asako/pdf/SSII2016_AsakoKanezaki_tutorial.pdf
- http://ros-robot.blogspot.jp/2011/08/pclapi-point-cloud-library-pcl-pcl-api.html

## color filter
- http://qiita.com/akachochin/items/47f1470565e76adb1880
