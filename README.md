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
