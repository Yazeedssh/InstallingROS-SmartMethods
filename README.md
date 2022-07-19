# Installing-ROS-on-Ubuntu_20.04--Smart-Methods--
## Ubuntu installation steps

After setting up and installing the VirtualBox from https://www.virtualbox.org

We have to install Ubuntu_20.04 on a virtual machine and to do that we well go to https://www.releases.ubuntu.com/20.04 
Press on " NEW " button to creat a virtual machine > Give a name to the machine > Control the memory size of machine the recommended size is 1024MB but we can increase it but better not cross the green line > We can leave the next setting at default " CREAT A VIRTUAL DISK NOW " > Also we can leave the next one at default " VDI (VIRTUAL DISK IMAGE) " > Choose " DYNAMICALLY ALLOCATED " > We can give up to 30.00 GB to the virtual hard disk. And we created our virtual machine.

After this we have to modify some settings by clicking on " Settings " > Go to " General " > " Advanced " and change the two options to " BIDRECTIONAL " > From " System " go to " Processor " and give the max but better not cross the green line > Same thing from " Display " we can max the " Video memory " > From " Storge " select the "EMPTY" DISK and click on the CD icon and choose " CHOOSE A DISK FILE " and open the Ubuntu_20.04 (iso) file > And we well keep the rest of the setting on default > The last step is to select the virtual machine and press on " START ". And now the installation well start. 

In the operating system WELCOME screen well appeares select " INSTALL UBUNTU " > Set up the language > Choose your favorite options and continue > We can choose " ERASE DISK AND INSTALL UBUNTU " because we are installing on a virtual box and nothing well effect or real operating system so we can just click on " INSTALL NOW " > set up your timezone and right your name and password for the system > After the installation we have to restart the system to get started. 

The last few steps is to edit the size to a full screen we well right some commandes so search for the " Terminal " and right :

```1- sudo apt-get update ```

> Enter your password :

```2- sudo apt-get upgrade ```

> Do you want to continue? [y\n] : yes 

It well start an update to the system and it may take a few minutes

```3- sudo apt install build-essential dkms linux-headers-$(uname -r)```

> Do you want to continue [y\n] : yes 

After it complete close the terminal window > click on "Devices" on the top > Choose " INSERT GUEST ADDITION CD IMAGE " > Click on " RUN " and type your password > It well start install guest addition modules > Press " Enter " and Restart the system and select " Power off " let it shut down and > Resize the screen and it well be full screen. 

## ROS installation steps 

Open Terminal and right the following commandes

### 1-Setup your sources.list

```sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'```

### 2-Set up your keys

```sudo apt install curl```

```curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -```

### 3-Installation

```sudo apt update```

There are 3 options in wiki.ros.org/Installation/Ubuntu  website you can pick how much of ROS you would like to install but this is the full version

### 4-Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages

```sudo apt install ros-noetic-desktop-full```

### 5-Setup the environment

```source /opt/ros/noetic/setup.bash```

#### We have to right this command every time we run ROS and to make it convenient we can run it automatically and source this script every time a new shell is launched

```echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc```

### 6- Check if ROS is installed correctly

``` roscore ```

#### If you want to install a specific package directly 

```sudo apt install ros-noetic-PACKAGE```

### 7-Dependencies for building packages

```sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential```

#### Initialize rosdep

```sudo apt install python3-rosdep```

```sudo rosdep init```

```rosdep update```

### Now you installed ROS and you can test your installation
