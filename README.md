# udm_if_gb
Ce package contient le package de la question 5 pour la partie 2 du TP4
Il permet de localiser le robot en faisant appel au service \global_localization et \request_nomotion_update


## Installation
Pour installer ce noeud il faut le cloner dans le dossier src de votre catkin workspace (catkin_ws).

```
cd catkin_ws/src
git clone https://github.com/IF488/udm_if_gb.git
catkin build
cd ..
source devel/setup.bash
```

## Execution
Dans un premier terminal, lancer Gazebo:

```
roslaunch turtlebot3_gazebo turtlebot3_world.launch
```

Dans un deuxième terminal, lancer le noeud de navigation:

```
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
```

Dans un troisième terminal, lancer le noeud global_localization.py

```
rosrun udm_ishan_gb global_localization.py
```

PS: La map utilisé est fourni dans le fichier. Placer map.yaml et map.pgm dans le fichier HOME de votre PC. Vous pouvez aussi placer la map dans un autre fichier à condition de changer l'argument dans la command ci-dessous.