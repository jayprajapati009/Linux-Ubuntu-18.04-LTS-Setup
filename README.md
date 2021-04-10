# Linux-Ubuntu-18.04-LTS-Setup
Basic setup for Linux Ubuntu 18.04 LTS (Recommended For ROS)

### To Update Linux
```
sudo apt-get update
```
Entering this command you'll be prompted to enter your password in the same terminal.
Take a note that while typing no character or '\*' will be displayed, as this is a password.
Simply type your password and press '**Enter Key**'
 
### To Upgrade Linux
```
sudo get-apt upgrade
```
While upgrade command you'll be asked to installing the packages, Simply pyress '**y**' and press '**Enter key**'

#### You can also run boths the commands at the same time 
```
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
```
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'
```

### Nvidia Drivers for Linux
[Click Here for the Link](https://www.nvidia.com/Download/driverResults.aspx/111596/en-us)

#### Alternatively, Go to **_Software And Updates_**, Go to **_Additional Drivers_**

![image](https://user-images.githubusercontent.com/60093076/114265279-94679200-9a0d-11eb-9ccc-6f3653436ea8.png)

Select the Recommended Drivers by ( ubuntu-drivers devices ) and Apply Changes

Install Synaptic Package Manager
Open Synaptic Package Manager
Search for openjdk-8-jre
search for ttf-mscorefonts-installer
Serch for ubuntu-restricted-extras
Mark For Installation
Apply ---------- Close

To get the media codecs (Using CLI)
sudo apt-get install ubuntu-restricted-extras

Open Synaptic Package Manager
Search for apt-xapian-index
Mark For Installation
Apply ---------- Close

Open Synaptic Package Manager
Search for microcode
Mark For Installation for Intel and AMD Microcode
Apply ---------- Close

To Reduce Swappiness
cat /proc/sys/vm/swappiness
gedit admin:///etc/sysctl.conf
enter the password
Scroll down the file and at the end write,
vm.swappiness = 10
save and close the file 
Reboot 
cat /proc/sys/vm/swappiness 
(Should be 10)

Open Disc
Select Hard Drive 
Select the Linux Partition 
Go to menu (Right Top)
Go to Drive Setting (ctrl + E)
Go to Write Cache
Enable It 

To Install Some Linux Packages
sudo apt-get install libavcodec-dev libsdl1.2-dev xsltproc libbullet-dev libsdl1.2-dev libgoogle-glog-dev protobuf-compiler python-wstool

To Set Up Git
sudo apt-get install git

To get Flatpak Supports (It enables the softwares which are not provided by Default App Store in Linux; Go to flathub website for more softwares and info)
sudo apt-get install flatpak
sudo apt-get install gnome-software-plugin-flatpak

To get the Flatpak softwares directly into the app store 
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

For removing unnecessary files and Maintaining System
sudo apt autoremove

--------------------------------------------------------------------------------------------------------------------------

GNOME EXTENSIONS

To install Gnome Tweaks
sudo apt-get install gnome-tweaks

To know version of GNOME Shell
gnome-shell --version

To install Gnome extensions 
sudo apt install gnome-shell-extensions

GNOME extensions Website
https://extensions.gnome.org/

To get the host connector
sudo apt install chrome-gnome-shell


