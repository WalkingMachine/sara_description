# sara_description

This repo contains the URDF model of sara     
You need to have the [https://github.com/WalkingMachine/robotiq_140_description] package to launch sara_description     

## Dependances
https://github.com/ridgeback/ridgeback_simulator.git
https://github.com/utecrobotics/robotiq.git


## To simulate with Rviz    
* roslaunch sara_description sara_description.launch test:=true
    * select base_link as the fixed frame
* rosrun rviz rviz     

## To simulate in Gazebo
* roslaunch sara_description sara_description.launch sim:=true     
* roslaunch sara_gazebo sara_gazebo.launch     


For any changes ask: red1laref     


## Citation
A.Rasouli, J.K. Tsotsos. "The Effect of Color Space Selection on Detectability and Discriminability of Colored Objects." arXiv preprint arXiv:1702.05421 (2017). http://data.nvision2.eecs.yorku.ca/3DGEMS/
