### Ros-Kinectic

## Install Ros Kinetic
Para instalar Ros Kinetic debemos abrir una terminal y desde alli pegar el siguiente comando:<br>
```bash 
sudo apt-get install ros-kinetic-full-desktop 
```
## Creating a map file
```
roscore
```
```
roslaunch turtlebot_bringup minimal.launch
```
```
roslaunch turtlebot_navigation gmapping_demo.launch
```
```
rosrun rviz rviz
```
<br>

### Operating your robot
To control your turtlebot with the keyboard:
```
roslaunch turtlebot_teleop keyboard_teleop.launch
```
Or if you want to use a PS3 joystick:<br> 
```
roslaunch turtlebot_teleop ps3_teleop.launch
```
[*Joystick Teleoperation*](http://library.isr.ist.utl.pt/docs/roswiki/turtlebot_teleop(2f)Tutorials(2f)TurtleBot(20)Joystick(20)Teleoperation.html)<br><br>

### Saving the map
Save map:<br>
```
rosrun map_server map_saver -f mymap
```


## Launching a map file
```
roscore
```
```
roslaunch turtlebot_bringup minimal.launch
```
```
roslaunch turtlebot_navigation amcl_demo.launch map_file:=/home/turtlebot/map.yaml
```
```
rosrun rviz rviz
```

## Install sound_play
sudo apt-get install ros-kinetic-sound-play<br> 

## Commands for sound_play
rosrun sound_play soundplay_node.py - lanzar el nodo del sound_play<br> 
/opt/ros/melodic/lib/sound_play/play.py PathDelArchivo volumen (maximo 1)<br> 
rosrun sound_play say.py "frase"<br> 
pactl -- set-sink-volume 0 500% - Para cambiar el sonido por defecto del ubuntu<br> 
https://anuragbhandari.com/coding-tech/fixing-headphone-jack-in-ubuntu-20-04-1755/<br> 

## Http Server with Python
```
source ~/venv/bin/activate
```

<br> 
Go with cd to the folder of the webpage<br>
<br>  
Launch a http server with python with this command:<br> 

```
python -m http.server
```

<br> 
Launch a socket for ros:<br> 

```
roslaunch rosbridge_server rosbridge_websocket.launch
```

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
