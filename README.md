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

![image](https://user-images.githubusercontent.com/85820553/128096051-f514e2b7-cb89-4d0a-9c6b-6f230e6ecc6d.png)


![image](https://user-images.githubusercontent.com/85820553/128096070-ff5c89bb-7783-4a56-81f9-a424f10df9c6.png)


1.5 Desktop-Full Install:
<!-->
      sudo apt install ros-melodic-desktop-full
      
 ![image](https://user-images.githubusercontent.com/85820553/128097688-d2e69847-64c3-4c26-bbb2-cebdd169ffb7.png)

      
 1.6 Environment setup:
 
<!-->
      echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc

![image](https://user-images.githubusercontent.com/85820553/128097817-52d30317-2010-4d3f-ae91-04cec9dcbbf3.png)



<!-->
      source ~/.bashrc
      
 ![image](https://user-images.githubusercontent.com/85820553/128097856-0eb6a773-eff8-4a2e-b871-a671e3afa16a.png)

 or
 
 <!-->
      source /opt/ros/melodic/setup.bash

or

<!-->
      echo "source /opt/ros/melodic/setup.zsh" >> ~/.zshrc


<!-->
      source ~/.zshrc


 1.7 Dependencies for building packages:



<!-->
      sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential
      
![image](https://user-images.githubusercontent.com/85820553/128097911-b827e9a4-8c74-4b12-979b-b8af07208af3.png)

      

1.7.1 Initialize rosdep:


<!-->
      sudo apt install python-rosdep

![image](https://user-images.githubusercontent.com/85820553/128097954-4839b9fb-6b3b-4e62-8d56-373a05ca65c9.png)



<!-->
      sudo rosdep init
      
 ![image](https://user-images.githubusercontent.com/85820553/128098001-77315e38-3fb9-4df8-906c-fe6c2f5e9915.png)

      
      
<!-->
      rosdep update

![image](https://user-images.githubusercontent.com/85820553/128098113-38c56887-7e19-451a-b87c-e9e03f000a4c.png)


![image](https://user-images.githubusercontent.com/85820553/128098131-2b025014-42c1-4e19-bff0-67f774b4284a.png)




- **Step-4:**
Create a workspace by using catkin_make with the following steps:

  1. Prerequisites:

<!-->
      source /opt/ros/melodic/setup.bash
      
 ![image](https://user-images.githubusercontent.com/85820553/128148959-e575584e-bbd9-48d8-b626-7ca56999729a.png)



1.1 Create and build a catkin workspace:


<!-->
      mkdir -p ~/catkin_ws/src

![image](https://user-images.githubusercontent.com/85820553/128149920-96bcc45c-3b33-4e97-a4fe-15f9d51805ab.png)



<!-->
      cd ~/catkin_ws/
      
 ![image](https://user-images.githubusercontent.com/85820553/128150073-4af9d6d2-d2f8-4c85-a5be-738817bb9b8b.png)



<!-->
      catkin_make

![image](https://user-images.githubusercontent.com/85820553/128150415-be5467af-8846-45ee-b6e6-1eba7babaf66.png)
 

![image](https://user-images.githubusercontent.com/85820553/128150460-3d20d17d-7876-45c4-9bba-8019db71e2b4.png)


![image](https://user-images.githubusercontent.com/85820553/128150519-2c882520-8428-4781-91af-f6c734949ab0.png)


![image](https://user-images.githubusercontent.com/85820553/128150590-9282e1dd-e617-423b-ae23-d7738944cc79.png)




<!-->
      echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
      
      
      
![image](https://user-images.githubusercontent.com/85820553/128152391-83c82d8a-8cf3-431d-bd8b-ecaa2f4ec5d8.png)



<!-->
      source ~/.bashrc

![image](https://user-images.githubusercontent.com/85820553/128152462-6887e0ea-8557-4112-af8a-1f590cf3bc31.png)



- **Step-5:**
Installing the package arduino_robot_arm:
