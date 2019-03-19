# sara_description
   
This repo contains the URDF model of sara     
You need to have the [https://github.com/WalkingMachine/robotiq_140_description] package to launch sara_description     

## To simulate with Rviz    
* roslaunch sara_description sara_description.launch test:=true
    * select base_link as the fixed frame
* rosrun rviz rviz     

## To simulate in Gazebo
* roslaunch sara_description sara_description.launch sim:=true     
* roslaunch sara_gazebo sara_gazebo.launch     
     
         
For any changes ask: red1laref     
