# Linux-Ubuntu-18.04-LTS-Setup
Basic setup for Linux Ubuntu 18.04 LTS (Recommended For ROS)

These are some suggested changes one should do while starting using Linux Ubuntu 18.04 especailly for ROS.

### To Update Linux
```sh
sudo apt-get update
```
Entering this command you'll be prompted to enter your password in the same terminal.

> Note: While typing `No character or *` will be displayed, as this is a password. 
Simply type your password and press '**Enter Key**'
 
### To Upgrade Linux
```sh
sudo get-apt upgrade
```
While upgrade command you'll be asked to installing the packages, Simply pyress '**y**' and press '**Enter key**'

#### You can also run boths the commands at the same time 
```sh
sudo apt-get update && sudo get-apt upgrade
```

### Additional Setting
#### Go to Software and Updates 

![image](https://user-images.githubusercontent.com/60093076/114265099-93823080-9a0c-11eb-8662-58a47b86908b.png)
![image](https://user-images.githubusercontent.com/60093076/114265127-b6ace000-9a0c-11eb-94ee-ada4af14b0bb.png)

Change the settings as per the images and close the dailougebox.

#### Go to ***Software Updater***
Update and Restart the system.

--------------------------------------------------------------------------------------------------------------------------

### Minimize in Dock
If you click on the icon of any application in the dock, it will not minimize, to fix this 
```sh
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

### Nvidia Drivers for Linux
[Click Here for the Link](https://www.nvidia.com/Download/driverResults.aspx/111596/en-us)

#### Alternatively, Go to **_Software And Updates_**, Go to **_Additional Drivers_**

![image](https://user-images.githubusercontent.com/60093076/114265279-94679200-9a0d-11eb-9ccc-6f3653436ea8.png)

Select the Recommended Drivers by ( ubuntu-drivers devices ) and Apply Changes

### Install Synaptic Package Manager

#### Open Synaptic Package Manager
Search for, 
```sh
openjdk-8-jre
```
Click on it and select **_Mark For Installation_**.

Search for,
```sh
ttf-mscorefonts-installer
```
Click on it and select **_Mark For Installation_**.

Search for,
```sh
ubuntu-restricted-extras
```
Click on it and select **_Mark For Installation_**.

Search for,
```sh
apt-xapian-index
```

Click on it and select **_Mark For Installation_**.

Search for,
```sh
microcode
```
Click on it and select **_Mark For Installation_** for **_Intel_** and **_AMD Microcode_**.

Click on apply and Close. 

#### Alternatively, To get the media codecs (Using CLI)
```sh
sudo apt-get install ubuntu-restricted-extras
```

### To Reduce Swappiness

To reduce the usage of the disk and use the RAM first

```sh
cat /proc/sys/vm/swappiness
```
```sh
gedit admin:///etc/sysctl.conf
```
Now, you'll be prompted to enter the password, after entering the password a file will be opened.
Scroll down the file and at the end write,
```sh
vm.swappiness = 10
```
Save and Close the file and Reboot Your System 

After rebooting open terminal and type,
```sh
cat /proc/sys/vm/swappiness 
```
The value should be 10

### To improve overall performance of Linux System

Open **_Disc_** App,
![image](https://user-images.githubusercontent.com/60093076/114265662-c0841280-9a0f-11eb-885b-0371df453ea8.png)

Select Hard Drive in which you have set up linux and Select the **_Linux Partition_**
![image](https://user-images.githubusercontent.com/60093076/114265677-ddb8e100-9a0f-11eb-80bb-5d2932cca507.png) 

Go to **_Menu_** (Right Top)and Go to **_Drive Setting (ctrl + E)_**
![image](https://user-images.githubusercontent.com/60093076/114265763-4607c280-9a10-11eb-97ea-e3450e17141f.png)

Go to **_Write Cache_**
Enable It 
![image](https://user-images.githubusercontent.com/60093076/114265786-6172cd80-9a10-11eb-9648-d6a18eeb74f5.png)
and Close the dailougebox.

### To Install Some Linux Packages
```sh
sudo apt-get install libavcodec-dev libsdl1.2-dev xsltproc libbullet-dev libsdl1.2-dev libgoogle-glog-dev protobuf-compiler python-wstool
```

### To Set Up Git
```sh
sudo apt-get install git
```

### To get Flatpak Supports 
It enables the softwares which are not provided by Default App Store in Linux; Go to flathub website for more softwares and info
```sh
sudo apt-get install flatpak
```
```sh
sudo apt-get install gnome-software-plugin-flatpak
```

### To get the Flatpak softwares directly into the app store 
```sh
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

### For removing unnecessary files and Maintaining System
```sh
sudo apt autoremove
```

--------------------------------------------------------------------------------------------------------------------------

## GNOME EXTENSIONS

### To install Gnome Tweaks
```sh
sudo apt-get install gnome-tweaks
```

### To know version of GNOME Shell
```sh
gnome-shell --version
````

### To install Gnome Extensions 
```sh
sudo apt install gnome-shell-extensions
```

#### GNOME Extensions Website
(https://extensions.gnome.org/)

### To get the Host Connector
```sh
sudo apt install chrome-gnome-shell
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## References

(1) https://averagelinuxuser.com/30-things-to-do-after-installing-ubuntu-18-04-lts/#1-configure-the-update-manager-and-repositories

(2) https://itsfoss.com/things-to-do-after-installing-ubuntu-18-04/

(3) https://www.youtube.com/watch?v=BLVtxpm5c2A

(4) https://www.youtube.com/watch?v=ynA_zv2eRzE 

(5) https://www.youtube.com/watch?v=CPDDBVeIyLw

(6) https://github.com/PranshuTople/Tools-For-ROS

(7) https://www.youtube.com/watch?v=g25yTWiuUcg

(8) https://itsfoss.com/gnome-shell-extensions/
