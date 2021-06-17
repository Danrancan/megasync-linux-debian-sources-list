# MEGAsync & MEGAcmd sources.list from mega.nz
#### This is a tutorial on how to add the official source repository for the MEGAsync and MEGAcmd apps developed by mega.nz, to your /etc/apt/sources.list (or preferably /etc/apt/sources.list.d/MEGA.nz.list) for installation & auto-upgrades of the corresponding apps, using a Linux Based Distribution.

1. Find Your Repo from mega.nz
Below is the main website link to find your distro specific version of your source repository for mega.nz and the megasync app. It is here to help you find the correct URI that corresponsds to your working distribution. DO NOT ADD THIS TO YOUR SOURCES LIST DIRECTLY!
    https://mega.nz/linux/MEGAsync/
    
2. Find the repository that corresponds to your distro
    EX: Debian 10 repository for megasync is located at 
    https://mega.nz/linux/MEGAsync/Debian_10.0/

3. To install these repositories and keep the megasync app updated on debian 10, when using the `sudo apt update && sudo apt upgrade` command, add the corresponding repository uri to your `/etc/apt/sources.list.d/MEGA.nz.list` file.

    `sudo nano /etc/apt/sources.list.d/MEGA.nz.list`


4. Then copy and paste your source directory into the megasync.list file that opens up, prefaced by a "deb " followed by a space and a "./".
     
     `deb https://mega.nz/linux/MEGAsync/Yourdistroname_yourdistroversionnumber/ ./`
     
      Example (Debian 10) "/etc/apt/sources.list.d/megasync.list" file
      
      `deb https://mega.nz/linux/MEGAsync/Debian_10.0/ ./`

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
