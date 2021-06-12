---
 title: How to Install Ubuntu Server on VirtualBox. 
 tags: [Ubuntu, VirtualBox]
 style: fill
 color: danger
 description: Hello Everyone, This blog will be deeply focusing on installation of Ubuntu server on VirtualBox.
---


## Introduction
In this blog I’ll show you how to install Ubuntu server version 20.04.2.0 LTS on Oracle’s VirtualBox 6.1.22. I will be explaining everything in a very simple way so that anyone can use this blog as an easy guide.

## VirtualBox
VirtualBox is open-source software for virtualizing the x86 computing architecture and is developed by Oracle Corporation. It supports the creation and management of virtual machines through which you can install a second operating system.
The operating system on which you install VirtualBox is called HOST(The regular operating system). The operating system you install within VirtualBox is called the GUEST. For this tutorial, I’ll be using Windows 10 as the host OS.

## Install VirtualBox
The first step you need to take is to install VirtualBox. I’ll not go into much details here, as there are perfect instructions for all of the main operating systems on the [VirtualBox homepage](https://www.virtualbox.org/). I’m going to download and install the latest version of virtualbox as 6.1.22 and ubuntu server as 20.04.2.0 LTS.

## Download Ubuntu Server
The second step is to download Ubuntu Server. You can do this from their [download page](https://ubuntu.com/download/desktop). This will download a 889 MB ISO file on your computer system.
Currently the latest LTS version is Ubuntu Server 20.04.2.0 and this is what I’ll be using. It is supported until April 2025 of free security and maintenance updates guaranteed.

## Create a new Virtual Machine 
Once you are done with installation, open the VirtualBox. The VirtualBox has an interface from which you will control all of your virtual machines.

<img src="/assets/images/vb1.png">

Now Click on New, give your virtual machine a name and the other fields will update accordingly.

<img src="/assets/images/vb2.png">


Click Next. Now in the wizard, select the amount of memory (RAM) in megabytes to be allocated to the virtual machine. I chose 2GB (2048 megabytes).

<img src="/assets/images/vb3.png">

Click Next and you will be directed to add a virtual hard disk to the new machine. Select ‘Create a virtual hard disk now’ and press Create.

<img src="/assets/images/vb4.png">

Here we have to choose the file type for the new virtual hard disk. Select VDI (VirtualBox Disk Image) and press Next.

<img src="/assets/images/vb5.png">

Now you will be asked ‘whether the new virtual hard disk should grow as it is used (dynamically allocated) or if it should be created at its maximum size (fixed size)’. Select dynamically allocated so that file may select it’s size according to the need and press Next.

<img src="/assets/images/vb6.png">

Select the size of the virtual hard disk in megabytes. The default size of 10GB should be plenty, but you can increase it if you need. Then click Create.

<img src="/assets/images/vb7.png">

The hard disk will be created and after a short while you will see yourself redirected to the VirtualBox Manager. You should be able to see your newly created virtual machine listed on the left. If not, then you must check what mistake you made in those steps.


## Install Ubuntu Server on the Virtual Machine

Open VirtualBox then go to settings > storage > controller: IDE and either you can choose Ubuntu ISO file from a disk or select the Ubuntu ISO file in the optical drive option and press Ok.

<img src="/assets/images/vb8.png">

Now select your virtual machine and press Start.
The Ubuntu installation process will now begin. It consists of thirteen steps and is very easy.
- The Welcome Screen
Here you should select your preferred language. I’m using English.

<img src="/assets/images/vb9.png">

- The Keyboard Configuration Screen
Here you should select a keyboard layout. As I’m using an English US keyboard, I asked Ubuntu to detect my layout, which it did with a couple of simple questions.

<img src="/assets/images/vb10.png">

- Network Connections Screen
Here Ubuntu will try to configure the standard network interface. Accept the default and select Done.

<img src="/assets/images/vb11.png">

- Configure Proxy Screen
If your system requires a proxy to connect to the internet (generally doesn’t), enter its details in the next dialogue. Then select Done.

<img src="/assets/images/vb12.png">

- Ubuntu Archive Mirror Screen
If you wish to use an alternative mirror for Ubuntu, you can enter its details here. Otherwise accept the default mirror by selecting Done.

<img src="/assets/images/vb13.png">

- Filesystem Setup Screen
The installer can guide you through partitioning an entire disk or, if you prefer, you can do it manually. If you choose to partition an entire disk you will still have a chance to review and modify the results before Ubuntu is installed. I selected Use An Entire Disk.
I was then taken to select my virtual machine’s hard disk as the disk to install to, before being shown a summary of what the installer would do. As this is a “destructive action”. I was asked to confirm my choice with Continue.

<img src="/assets/images/vb14.png">

<img src="/assets/images/vb15.png">

<img src="/assets/images/vb16.png">

- Profile Setup Screen
Here you are required to enter:
         - Your (real) name
         - Your server’s name
         - Your username
         - Password 

<img src="/assets/images/vb17.png">
 
- SSH Setup Screen
Here we can install the OpenSSH [server package](https://help.ubuntu.com/lts/serverguide/openssh-server.html). We’ll need this to connect to the virtual machine via SSH later, so make sure to select it.
You can also import your SSH keys from GitHub or Launchpad. I selected No for this option. Now press Done.

<img src="/assets/images/vb18.png">
 
- Featured Server Snaps screen
You can select from a list of popular snaps to install on your system if you need. [Snaps](https://tutorials.ubuntu.com/tutorial/basic-snap-usage#0) are self-contained software packages that work across a range of Linux distributions. I didn’t select any and press Done to go to the next page.

<img src="/assets/images/vb19.png">

Now you will see the screen where  installation is being processed. This may take a while.

<img src="/assets/images/vb20.png">

And now the installation is complete.

<img src="/assets/images/vb21.png">

You’re good to go. Just reboot.

THANK YOU FOR READING MY BLOG :)

