
Launch Simulation World
---------------------------------------------

In the previous SLAM section, TurtleBot3 World is used to create a map. The same Gazebo environment will be used for Navigation.

$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch.

![لقطة الشاشة 2022-08-14 043147](https://user-images.githubusercontent.com/107875617/184557913-acb30def-5cb3-4787-996d-d344e6dc7aee.jpg)


Run Navigation Node
----------------------------------------------

Open a new terminal from Remote PC with Ctrl + Alt + T and run the Navigation node.

$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml



![لقطة الشاشة 2022-08-15 015711](https://user-images.githubusercontent.com/107875617/184557954-b73decdf-370f-49aa-b7fa-4ce0f146d0a2.jpg)


Estimate Initial Pose
---------------------------------------------

Initial Pose Estimation must be performed before running the Navigation as this process initializes the AMCL parameters that are critical in Navigation. TurtleBot3 has to be correctly located on the map with the LDS sensor data that neatly overlaps the displayed map.

Click the 2D Pose Estimate button in the RViz menu.

Click on the map where the actual robot is located and drag the large green arrow toward the direction where the robot is facing.


Set Navigation Goal
--------------------------------------------

Click the 2D Nav Goal button in the RViz menu.
Click on the map to set the destination of the robot and drag the green arrow toward the direction where the robot will be facing

![1444-01-17-01-14-30](https://user-images.githubusercontent.com/107875617/184558078-c3f54c5d-f2a8-4ae1-b35b-5dee47038043.gif)

