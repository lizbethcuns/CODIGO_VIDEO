# CODIGO_VIDEO
# ----------------------------> Generando un mapa usando el paquete slam_toolbox <-------------------------------------

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
# 
# 
# 
