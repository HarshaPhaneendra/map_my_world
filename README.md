# map_my_world
This Project is of "Mapping environment world", part of Udacity Nano Degree Program "Robotics Engineer". 

## Build and Run
### Terminal 1
* Download and Build the project
```
cd /home/<username>/catkin_ws/src
git clone git@github.com:HarshaPhaneendra/map_my_world.git
cd ..
catkin_make
source devel/setup.bash
```
* Launch 'world.launch', which includes 'rviz_config' file.
```
roslaunch my_world world.launch
```

### Terminal 2
* Run Teleop node to handel controls of robot. 
```
cd /home/<username>/catkin_ws
source devel/setup.bash
roslaunch my_robot teleop.launch
```
### Terminal 3 
* Launch 'mapping.launch' or 'localization.launch' file to generate environment map world. 
```
cd /home/<username>/catkin_ws
source devel/setup.bash
roslaunch my_robot mapping.launch
```
### Terminal 4 
* To analyse the saved 'rtabmap.db' files.
* "rtabmap_4.db" - Using "mapping.launch", robot has travelled the most to get high loop enclosure counts and better 3D map.

```
rtabmap-databaseViewer rtabmap_4.db
```

