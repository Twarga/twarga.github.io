---
title: "Installing GNS3 on Linux: A Comprehensive Guide"
date: 2024-10-21
categories: [Blog, Cybersecurity, Networking]
tags: [Blog, GNS3, Linux, Ubuntu, Fedora, Arch Linux, OpenSUSE, Virtualization, IT Skills, Networking, CCNA, CompTIA Network+]

---

# Installing GNS3 on Linux: A Comprehensive Guide
The installation process for GNS3 on Linux varies slightly depending on the distribution. For Ubuntu/Debian-based systems, it can be done using a PPA repository, while for other distributions like Fedora, Arch, or openSUSE, you will use the default package manager or install from the official GNS3 website. Below is a step-by-step guide to help you install GNS3 on any Linux distribution.

## Step 1 : Add GNS3 Repository or Use Package Manager 
For Ubuntu/Debian-based distributions:
```bash
sudo apt update
sudo add-apt-repository ppa:gns3/ppa

```
For Fedora:

```bash
sudo dnf install gns3-gui gns3-server 
```
For Arch Linux (using AUR):
```bash
yay -S gns3-gui gns3-server
```
For openSUSE:
```bash
sudo zypper install gns3-gui gns3-server
```


> If GNS3 is not available in your distribution's package manager, you can download it manually from the GNS3 website.

![sudo apt update ](assets/GNS3/1.png)
![add ppa ](assets/GNS3/2.png)
Input your user password and press [ENTER] to continue if prompted.

## Step 2 : Install GNS3 GUI and GNS3 Server 
After adding the repository or confirming availability in your package manager, update your package list and install the required packages.

For Ubuntu/Debian-based distributions:
```bash
sudo apt update
sudo apt install gns3-gui gns3-server

```

For Fedora
```bash
sudo dnf install gns3-gui gns3-server
```

For Arch Linux (using AUR):
```bash
yay -S gns3-gui gns3-server
```

For openSUSE:
```bash
sudo zypper install gns3-gui gns3-server

```
A number of packages will be installed in your system; press the y key to accept the installation when prompted. You may also be prompted to allow non-root users to use Wireshark for packet capturing. Make sure to select Yes if needed.

![install gns3](assets/GNS3/5.png)

Allow non-root users to use wireshark:
![press Yes](assets/GNS3/6.png)

## Step 3 : Install IOU Support (Optional)
IOU (IOS over Unix) is an internal Cisco tool for simulating the ASICs in Cisco switches, allowing you to work with Layer 2 switching in your labs.

For Ubuntu/Debian 
```bash
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install gns3-iou

```

For Fedora
```bash
sudo dnf install gns3-iou
```

For Arch Linux (AUR)
```bash
yay -S gns3-iou
```
For openSUSE:
```bash
sudo zypper install gns3-iou
```

## Step 4 : Launch GNS3
Once GNS3 is installed, you can launch it using the terminal on any Linux distribution:
```bash
gns3
```
On the first page of the setup, select "Run the appliances on my computer".
![on my configuration](assets/GNS3/8.png)


On the next screen, confirm the local server configuration.
![local Server](assets/GNS3/9.png)

Complete the setup, and you are ready to start using GNS3 on Linux.

![start gns3 on Linux](assets/GNS3/10.png)

Voila! Your GNS3 installation is now complete and ready for use.


