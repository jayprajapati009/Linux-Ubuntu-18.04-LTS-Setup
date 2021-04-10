# Linux-Ubuntu-18.04-LTS-Setup
Basic setup for Linux Ubuntu 18.04 LTS (Recommended For ROS)

### To Update Linux
```
sudo apt-get update
```
 
### To Upgrade Linux
```
sudo get-apt upgrade
```
While upgrade command you'll be asked to installing the packages, Simply pyress '**y**' and press '**Enter key**'

#### You can also run boths the commands at the same time 
```
sudo apt-get update && sudo get-apt upgrade
```

Go to Software and Updates 
and change the setting as per the Video 

Go to App Updater
Update
Restart

--------------------------------------------------------------------------------------------------------------------------

If you click on the icon of any application in the dock, it will not minimize, to fix this 
gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'

Nvidia Drivers for Linux
https://www.nvidia.com/Download/driverResults.aspx/111596/en-us
Also Go to Software And Updates 
Additional Drivers 
Select the Recommended Drivers by ( ubuntu-drivers devices )
Apply

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


