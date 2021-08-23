### Ros-Kinectic

## Install Ros Kinetic
Para instalar Ros Kinetic debemos abrir una terminal y desde alli pegar el siguiente comando:
sudo apt-get install ros-kinetic-full-desktop

## Launching a map file
roscore 
roslaunch turtlebot_bringup minimal.launch
roslaunch turtlebot_navigation amcl_demo.launch map_file:=/home/turtlebot/map.yaml
rosrun rviz rviz

## Install sound_play
sudo apt-get install ros-kinetic-sound-play

## Commands for sound_play
rosrun sound_play soundplay_node.py - lanzar el nodo del sound_play
/opt/ros/melodic/lib/sound_play/play.py PathDelArchivo volumen (maximo 1)
rosrun sound_play say.py "frase"
pactl -- set-sink-volume 0 500% - Para cambiar el sonido por defecto del ubuntu
https://anuragbhandari.com/coding-tech/fixing-headphone-jack-in-ubuntu-20-04-1755/

## Http Server with Python
source ~/venv/bin/activate
Go with cd to the folder of the webpage
Launch the server with python -m http.server
roslaunch rosbridge_server rosbridge_websocket.launch
