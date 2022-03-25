### Ros-Kinectic

## Install Ros Kinetic
Para instalar Ros Kinetic debemos abrir una terminal y desde alli pegar el siguiente comando:
sudo apt-get install ros-kinetic-full-desktop

## Launching a map file
roscore<br> 
roslaunch turtlebot_bringup minimal.launch<br> 
roslaunch turtlebot_navigation amcl_demo.launch map_file:=/home/turtlebot/map.yaml<br> 
rosrun rviz rviz<br> 

## Install sound_play
sudo apt-get install ros-kinetic-sound-play<br> 

## Commands for sound_play
rosrun sound_play soundplay_node.py - lanzar el nodo del sound_play<br> 
/opt/ros/melodic/lib/sound_play/play.py PathDelArchivo volumen (maximo 1)<br> 
rosrun sound_play say.py "frase"<br> 
pactl -- set-sink-volume 0 500% - Para cambiar el sonido por defecto del ubuntu<br> 
https://anuragbhandari.com/coding-tech/fixing-headphone-jack-in-ubuntu-20-04-1755/<br> 

## Http Server with Python
source ~/venv/bin/activate<br> 
Go with cd to the folder of the webpage<br> 
Launch the server with python -m http.server<br> 
roslaunch rosbridge_server rosbridge_websocket.launch<br> 

## Creating a map file
roscore<br> 
roslaunch turtlebot_bringup minimal.launch<br> 
roslaunch turtlebot_navigation gmapping_demo.launch<br> 
rosrun rviz rviz<br> 
roslaunch turtlebot_teleop keyboard_teleop.launch<br>
Or if you want to use a PS3 joystick:<br> 

```diff
roslaunch turtlebot_teleop ps3_teleop.launch
```
<!-- http://library.isr.ist.utl.pt/docs/roswiki/turtlebot_teleop(2f)Tutorials(2f)TurtleBot(20)Joystick(20)Teleoperation.html -->



## Listener to the commands
python listener.py<br>
python go_one_point.py<br>
rostopic echo/recognizer/output<br>

## ROS2D & NAV2DJS
To see an arrow with robot_pose, use this command:<br>
rosrun robot_pose_publisher robot_pose_publisher<br>

## RosnodeJS
rosnodejs also provides the ability to dynamically create message classes on the fly without the need to run catkin_make
```diff
rosnodejs.initNode('my_node',
                   { onTheFly: true });
```
