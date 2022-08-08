# --Write the steps to perform the installation of ROS
1- Download VirtualBox Download Windows version https://WWW.virtualbox.org/wiki/Downloads
2- Install Ubuntu 16.04 LTS on it https://releases.ubuntu.com/16.04/ 64bit PC
3- New -> Name : ros_os->Next
We enter the site to install the ROS command https://s-m.com.sa/ros.txt
First, we open the command execution window by searching for the word Terminal
We will configure the sources.list file for Ubuntu software updates so that the system can download and install ROS release packages. This is done by copying the following command on the Terminal and pressing Enter

sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" >
 /etc/apt/sources.list.d/ros-latest.list'

After that we add the keys for the ROS version by copying the following command

    sudo apt install curl # if you haven't already installed curl
    curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

After you have configured the operating system settings for ROS installation. In this step, we will install ROS on the system, but before that we will first make sure that all updates for the operating system are installed using the following command on the Terminal:

sudo apt update

Wait for the download to finish:
Then we will now install the ROS

The full version ( ros-melodic-desktop-full ) which comes with many libraries and 3D/2D emulators.
By copying the following command on the Terminal


sudo apt install ros-melodic-desktop-full


Then press Enter to download the bots operating system, where it will ask us to agree to download the files as shown in the images below. For approval, we type the letter Y on the command window and then press Enter
Immediately after that, it starts downloading and then installing it on the system

After we have finished downloading and installing the ROS operating system, we move on to the last step, which is to prepare and configure the ROS environment so that we can work on it. First, we register the enviroment variables on the system so that we can execute the ROS commands each time we 
Open the Terminal using the following command:

echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc

We will install some plugins and utilities that we need while working in ROS, for example the rosinstall tool that allows us to download and install libraries and code for bots. These tools are installed using the following command

sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

Before we can use these tools and employ them, we first need to activate them by executing this command on the Terminal

sudo apt install python-rosdep

Then we run this command

sudo rosdep init

Finally, we run the following command on the Terminal

rosdep update
And with this, we have completed the process of installing the ROS robot operating system on the UBUNTU
 <img width="383" alt="png" src="https://user-images.githubusercontent.com/108256116/183362374-99f269fe-3738-4f20-9ab0-08b56356d10b.png">
 #  References:-
 http://wiki.ros.org/noetic/Installation/Ubuntu

