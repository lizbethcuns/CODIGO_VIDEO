# CODIGO_VIDEO
# ----------------------------> Generando un mapa usando el paquete slam_toolbox <-------------------------------------
source ~/turtlebot4_ws/install/setup.bash



#Primero, instala turtlebot4_navigation:
sudo apt install ros-humble-turtlebot4-navigation

#Luego ejecuta SLAM. Se recomienda ejecutar SLAM sincrónico en una PC remota para obtener un mapa de mayor resolución.
ros2 launch turtlebot4_navigation slam.launch.py

# -------------- En otra terminal -------------
export LIBGL_ALWAYS_SOFTWARE=true

#Lanza Rviz2 Para visualizar el mapa, lanza Rviz2 con el archivo launch view_robot.
ros2 launch turtlebot4_viz view_robot.launch.py

# -------------- En otra terminal -------------
export LIBGL_ALWAYS_SOFTWARE=true

#Se lanza el Ignition Gazebo 
ros2 launch turtlebot4_ignition_bringup turtlebot4_ignition.launch.py --humble

# ------------- se empieza a mover el robot con las flechas  -------------
#EN el gazebo , en el segundo que es vertical, se cambia el valor de 1.00 se cambia a 2.10

# -------------- En otra terminal -------------
source /opt/ros/humble/setup.bash

# Se revisa el topic list que este /cmd_vel 
ros2 topic list

# Se visualizan los dos mapas en movimiento se usa el comando de moverlo desde la temrinal 

ros2 topic pub /cmd_vel geometry_msgs/Twist '{linear: {x: 0.7 , y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 0.0}}'

# -------------- En otra terminal -------------
source /opt/ros/humble/setup.bash
# Guardar el Mapa
cd turtlebot4_ws
cd src

ros2 service call /slam_toolbox/save_map slam_toolbox/srv/SaveMap "name:
  data: 'map_name'"                                              EN ESTA LINEA HAY QUE PONERLE EL NOMBRE QUE YO QUIERA
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
# 
