# megasync-linux-debian-sources-list
##### This is the official source repository for the megasync app by mega.nz. 
##### This is relatively undocumented so I am puting it out there for others.

##### This is the main website link to find your distro specific version of your source repository for mega.nz and the megasync app. 
##### DO NOT ADD THIS TO YOUR SOURCES LIST. 
##### IT IS ONLY TO HELP YOU FIND THE CORRECT URI FOR YOUR SOURCES LIST. 
https://mega.nz/linux/MEGAsync/


### HOW TO ADD YOUR CORRESPONDING REPOSITORY TO YOUR SOURCES LIST FOR AUTO-UPDATING:
# EX: Debian 10 repository for megasync
https://mega.nz/linux/MEGAsync/Debian_10.0/

#### To install these repositories and keep the megasync app updated on debian 10, when using 
#### the "sudo apt update && sudo apt upgrade" command, add the corresponding 
#### repository uri to "/etc/apt/sources.list.d/megasync.list"
sudo mkdir -p /etc/apt/sources.list.d/
sudo nano /etc/apt/sources.list.d/megasync.list

# Then copy and paste your source directory into the megasync.list file that 
# opens up, followed by a space and a ./
$ https://mega.nz/linux/MEGAsync/Yourdistroname_yourdistroversionnumber/ ./

# Example (Debian 10) "/etc/apt/sources.list.d/megasync.list" file
$ https://mega.nz/linux/MEGAsync/Debian_10.0/ ./

# Hit "ctrl x" and save your file

# Update your repositories and install megasync
$ sudo apt update && sudo apt upgrade && sudo apt install megasync

# You now have megasync installed on Debain 10

# Here are a few other repository addresses:

# Raspian 10 megasync repository
https://mega.nz/linux/MEGAsync/Raspbian_10.0/

# Ubuntu 20.10 megasync repository
https://mega.nz/linux/MEGAsync/xUbuntu_20.10/

# Ubuntu 20.04 megasync repository
https://mega.nz/linux/MEGAsync/xUbuntu_20.04/

# Ubuntu 18.04 megasync repository
https://mega.nz/linux/MEGAsync/xUbuntu_18.04/

# Fedora 33 megasync repository
https://mega.nz/linux/MEGAsync/Fedora_33/

# Arch linux megasync repository
https://mega.nz/linux/MEGAsync/Arch_Extra/

# Cent OS 8 megasync repository
https://mega.nz/linux/MEGAsync/CentOS_8/
