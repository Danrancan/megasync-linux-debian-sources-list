# The Up-To-Date Guide of Mega.nz apt repositories, signing keys, and sources.list for MEGAsync & MEGAcmd on Debian

## This is a tutorial on how to add the official source repository for the MEGAsync and MEGAcmd apps developed by mega.nz, to your /etc/apt/sources.list (or preferably /etc/apt/sources.list.d/mega.nz.list) for installation & auto-upgrades of the corresponding apps, using a Debian Based Distribution.

### 1. Find Your Repo from mega.nz
Below is the main website link to find your distro specific version of your source repository for mega.nz and the megasync app. It is here to help you find the correct URI that corresponsds to your working distribution. DO NOT ADD THIS TO YOUR SOURCES LIST DIRECTLY! Now, go to the link in your web browser.

    [https://mega.nz/linux/repo/](https://mega.nz/linux/repo/)
    
### 2. Find the repository that corresponds to your distro
    
    Syntax: Go to https://mega.nz.linux/repo/YOUR_DISTRO_OF_CHOICE_HERE/
    
    Example 1: Debian 11 repository for mega apps is located at: 
    [https://mega.nz/linux/repo/Debian_11/](https://mega.nz/linux/repo/Debian_11/)

    Example 2: Debian 12 repository for mega apps is located at:
    [https://mega.nz/linux/repo/Debian_12/](https://mega.nz/linux/repo/Debian_12/)
    
### 3. Download the gpg release key file from the Debian Repository and dearmor it, then put it in your /etc/apt/keyrings folder.

    Syntax:
    `curl -fsSL https://mega.nz/linux/repo/YOUR_DISTRO_OF_CHOICE_HERE/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/mega.nz.gpg`

    Example 1: Debian 11
    `curl -fsSL https://mega.nz/linux/repo/Debian_11/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/mega.nz.gpg`

    Example 2: Debian 12
    `curl -fsSL https://mega.nz/linux/repo/Debian_12/Release.key | sudo gpg --dearmor -o /etc/apt/keyrings/mega.nz.gpg`

### 4. To install these repositories and keep the megasync app updated on debian 11 or Debian 12, when using the `sudo apt update && sudo apt upgrade` command, add the corresponding repository uri to your `/etc/apt/sources.list.d/mega.nz.list` file.

    Syntax:
    `echo "deb [arch=amd64,arm64 signed-by=/etc/apt/keyrings/mega.nz.gpg] https://mega.nz/linux/repo/YOUR_DISTRO_OF_CHOICE_HERE/ ./" | sudo tee /etc/apt/sources.list.d/mega.nz.list > /dev/null`
    
    Example 1: Debian 11
    `echo "deb [arch=amd64,arm64 signed-by=/etc/apt/keyrings/mega.nz.gpg] https://mega.nz/linux/repo/Debian_11/ ./" | sudo tee /etc/apt/sources.list.d/mega.nz.list > /dev/null`

    Example 2: Debian 12
    `echo "deb [arch=amd64,arm64 signed-by=/etc/apt/keyrings/mega.nz.gpg] https://mega.nz/linux/repo/Debian_12/ ./" | sudo tee /etc/apt/sources.list.d/mega.nz.list > /dev/null`

### 5. Update your repositories
  
    `sudo apt update && sudo apt upgrade`

### 6. Install your desired MEGA Applications

    Example 1: MEGAsync
    `sudo apt install megasync`

    Example 2: MEGAcmd
    `sudo apt install megacmd`

    Example 3: Nautilus Support for MEGAsync
    `sudo apt install nautilus-megasync`

    Example 4: Nemo Support for MEGAsync
    `sudo apt install nemo-megasync`

    Example 5: Dolphin Support for MEGAsync
    `sudo apt install dolphin-megasync`

    Example 6: Thunar Support for MEGAsync
    `sudo apt install thunar-megasync`
    
### FINISHED: You have now properly installed MEGA Apps on your Debian Distribution


# Here are a few other repository addresses:

#### Raspian 10 MEGA repository
[https://mega.nz/linux/MEGAsync/Raspbian_10.0/](https://mega.nz/linux/repo/Raspbian_10.0/)

#### Raspian 11 MEGA repository
[https://mega.nz/linux/repo/Raspbian_11/](https://mega.nz/linux/repo/Raspbian_11/)

#### Ubuntu 20.04 MEGA repository
[https://mega.nz/linux/repo/xUbuntu_20.04/](https://mega.nz/linux/repo/xUbuntu_20.04/)

#### Ubuntu 22.04 MEGA repository
[https://mega.nz/linux/repo/xUbuntu_22.04/](https://mega.nz/linux/repo/xUbuntu_22.04/)

#### Fedora 39 MEGA repository
[https://mega.nz/linux/MEGAsync/Fedora_33/](https://mega.nz/linux/repo/Fedora_39/)

#### OpenSuse Leap 42.3
[https://mega.nz/linux/repo/openSUSE_Leap_42.3/](https://mega.nz/linux/repo/openSUSE_Leap_42.3/)
