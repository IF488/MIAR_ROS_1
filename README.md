# MIAR_ROS_1
Robotique Industriel TP

## udm_urdf
Ce package est le résultat du TP "Créer un urdf et le mettre en mouvement". Ce TP est une introduction au URDF (Unified Robot Description Format) qui 
est la façon dans ROS de décrire un robot.

### Installation
Pour installer ce noeud il faut le cloner dans le dossier src de votre catkin workspace (catkin_ws).

```
cd catkin_ws/src
git clone https://github.com/IF488/MIAR_ROS_1.git
catkin build
cd ..
source devel/setup.bash
```
### Execution
Pour visualiser, il faut executer le code suivant dans le terminal de votre worspace:

```
roslauch udm_urdf visualize_urdf.launch  model:='$(find udm_urdf)/urdf/main.urdf'
```
## TPRI3
Ce folder contient trois package pour le TP "Animer un urdf via Move it". 

### Installation
Pour installer ces noeuds, il faut placer les trois packages se trouvant dans le fichier TPRI3 dans le dossier src de votre catkin workspace. Il faut ensuite ouvrir un terminal a partir de votre catkin workspace et executer le code suivant:

```
catkin build
source devel/setup.bash
```

### Execution
Pour executer il faut ouvrir trois terminal a partir de votre catkin workspace, dans le premier terminal executer le code suivant:

```
source devel/setup.bash
roslaunch udm_hand_moveit_config demo.launch
```

#### Cinématique directe
Dans le deuxième terminal exécuter le code suivant:

```
source devel/setup.bash
rosrun udm_hand_control direct_server.py
```

Dans le troisième terminal exécuter le code suivant:

```
source devel/setup.bash

rosservice call /direct_service "joint_goal1:
  data: -0.8
joint_goal2:
  data: -0.8
joint_goal3:
  data: -0.8
group:
  data: 'ring'"
```
NB: Les noms des groups sont: thumb, index, middle, ring, pinky

#### Cinématique inverse
Dans le deuxième terminal exécuter le code suivant:

```
source devel/setup.bash
rosrun udm_hand_control inverse_server.py
```

Dans le troisième terminal exécuter le code suivant:

```
source devel/setup.bash

rosservice call /inverse_service "orientation:
  data: 1.0
posex:
  data: 0.1
posey:
  data: 0.4
posez:
  data: 0.2
group:
  data: 'ring'"
```
NB: Les noms des groups sont: thumb, index, middle, ring, pinky
