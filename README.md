# Installing Robot Arm Packages in ROS
## Steps of installing robot arm packages in Robot Operating System (ROS):

- **Step-1:**
            Install Oracle VM VirtualBox from [this link](https://www.virtualbox.org/wiki/Downloads).



- **Step-2:**
            Install Ubuntu 18.04 from [this link](https://releases.ubuntu.com/18.04).
            
   Follow [this video](https://youtu.be/QbmRXJJKsvs) steps to install Ubuntu 18.04 on Oracle VM VirtualBox



- **Step-3:**
Install ROS Melodic packages with the following steps:

  1- Installation:
  
   1.1 Configure Ubuntu repositories to allow "restricted," "universe," and "multiverse", [use this link to help you](https://youtu.be/NoVWMSCEPoQ).

   1.2 Setup sources.list using the following command:
      
      sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   
   1.3 Setup keys:

<!-->
      sudo apt install curl
      
<!-->
      curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add - 
      
      
   1.4 Setup keys:

<!-->
      sudo apt update

   
