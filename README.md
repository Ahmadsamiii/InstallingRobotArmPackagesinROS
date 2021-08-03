# Installing Robot Arm Packages in ROS
## Steps of installing robot arm packages in Robot Operating System (ROS):

- **Step-1:**
            Install Oracle VM VirtualBox from [this link](https://www.virtualbox.org/wiki/Downloads).
            
     ![image](https://user-images.githubusercontent.com/85820553/128093150-99c207d5-3751-4e01-809d-2661c634f070.png)




- **Step-2:**
            Install Ubuntu 18.04 from [this link](https://releases.ubuntu.com/18.04).
            
   Follow [this video](https://youtu.be/QbmRXJJKsvs) steps to install Ubuntu 18.04 on Oracle VM VirtualBox
   
   ![image](https://user-images.githubusercontent.com/85820553/128093284-1557b366-e695-40c7-9f92-3767148c40b7.png)




- **Step-3:**
Install ROS Melodic packages with the following steps:

  1- Installation:
  
   1.1 Configure Ubuntu repositories to allow "restricted," "universe," and "multiverse", [use this link to help you](https://youtu.be/NoVWMSCEPoQ).
   
   ![image](https://user-images.githubusercontent.com/85820553/128093579-49b1307b-5dd3-48fe-8325-cbe3e4f4744e.png)


   1.2 Setup sources.list using the following command:
      
      sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
      
   ![image](https://user-images.githubusercontent.com/85820553/128093613-bfdcd5ee-0ed6-43f2-bec0-985b727fd266.png)

   
   1.3 Setup keys:

<!-->
      sudo apt install curl

![image](https://user-images.githubusercontent.com/85820553/128093689-d540a9ad-8daa-4334-91c8-4ca64323c64c.png)

      
<!-->
      curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add - 
      
   ![image](https://user-images.githubusercontent.com/85820553/128095455-3fd4a162-ec6f-41ea-8ec1-47ef1338ee20.png)

      
      
   1.4 Setup keys:

<!-->
      sudo apt update

   
