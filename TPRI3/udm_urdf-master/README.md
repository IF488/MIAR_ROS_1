# udm_urdf

Ce package contient plusieurs fichier urdf ainsi qu'un launch file qui permet de visualiser les urdf.

# Installation

Pour installer ce package il faut le cloner dans le dossier src de votre catkin workspace (catkin_ws)

```sh
cd catkin_ws/src
git clone https://github.com/Kramoth/udm_urdf.git
catkin build
cd ..
source devel/setup.bash
```

# Execution

Pour visualiser les urdf, apres avoir sourcer le setup.bash

```sh
roslaunch udm_urdf check_urdf.launch
```

Par defaut, le fichier box.urdf sera afficher.

Dans le dossier urdf du package, il y a box.urdf, cylinder.urdf, sphere.urdf, mesh.urdf et main.urdf

Pour afficher main.urdf, dans un terminal taper la commande suivante:

```sh
roslaunch udm_urdf check_urdf.launch model:='$(find udm_urdf)/urdf/main.urdf'
```

Attention les single quote sont importants.