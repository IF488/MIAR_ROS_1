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
Pour installer ces noeuds, il faut placer les trois packages se trouvant dans le fichier TPRI3 dans le dossier src de votre catkin workspace. 

### Execution
Pour executer il faut ouvrir deux terminal a partir de votre catkin workspace, dans le premier terminal executer le code suivant:

```
roslaunch udm_hand_moveit_config demo.launch
```

Dans le deuxième terminal exécuter le code suivant:

```
roslaunch udm_hand_control direct_cinematique.launch
```
