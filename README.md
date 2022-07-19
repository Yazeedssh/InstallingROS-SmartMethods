# Installing-ROS-on-Ubuntu_20.04--Smart-Methods--
# Ubuntu installation steps

After setting up and installing the VirtualBox from https://www.virtualbox.org

We have to install Ubuntu_20.04 on a virtual machine and to do that we well go to https://www.releases.ubuntu.com/20.04 
Press on " NEW " button to creat a virtual machine > Give a name to the machine > Control the memory size of machine the recommended size is 1024MB but we can increase it but better not cross the green line > We can leave the next setting at default " CREAT A VIRTUAL DISK NOW " > Also we can leave the next one at default " VDI (VIRTUAL DISK IMAGE) " > Choose " DYNAMICALLY ALLOCATED " > We can give up to 30.00 GB to the virtual hard disk. And we create our virtual machine.

After this we have to modify some setting by clicking on " Settings " > Go to " General " > " Advanced " and change the two options to " BIDRECTIONAL " > From " System " go to " Processor " and give the max but better not cross the green line > Same thing from display we can max the " Video memory " > From " Storge " select the "EMPTY" DISK and click on the CD icon and choose " CHOOSE A DISK FILE " and open the Ubuntu_20.04 iso file > And we well keep the rest of the setting on default > The last step is to select the virtual machine and press on " START ". And now the installation well start. 

In the operating system WELCOME screen well appeare select " INSTALL UBUNTU " > Set up the language > Choose your favorite options and continue > We can choose " ERASE DISK AND INSTALL UBUNTU " because we are installing on a virtual box and nothing well effect or real operating system so we can just click on " INSTALL NOW " > set up your timezone and right your name and password for the system > After the installation we have to restart the system to get started. 

The last few steps is to edit the size to full screen we well right some commande so search for the " Terminal " and right :

1- sudo apt-get update 

Enter your password :

2- sudo apt-get upgrade 

Do you want to continue? [y\n] : yes 

It well start an update to the system and it may take a few minutes

3- sudo apt install build-essential dkms linux-headers-$(uname -r)

Do you want to continue [y\n] : yes 

After it complete close the terminal window > click on "Devices" on the top > Choose " INSERT GUEST ADDITION CD IMAGE " > Click on " RUN " and type your password > It well start install guest addition modules > Press " Enter " and Restart the system and select " Power off " let it shut down and > Resize the screen and it well be full screen. 
