# Demo Oracle Database + Oracle Linux + macOS UTM QEMU

Demonstration of:

* Oracle Database 19c Aarch64

* Oracle Linux 8 Aarch64

* macOS UTM QEMU emulator on macOS 14.1 Arm M1

Feedback welcome.


## Download Oracle Linux

Oracle Linux 8 Aarch64 DVD ISO is a full installation disk image. It can work with system emulators and virtual machine hosts.

[Download Oracle Linux 8 Aarch64 DVD ISO](https://yum.oracle.com/ISOS/OracleLinux/OL8/u9/x86_64/OracleLinux-R8-U9-x86_64-dvd.iso).


## Download macOS UTM QEMU

UTM is a user-friendly full-featured system emulator and virtual machine host for iOS and macOS. UTM enables you to run Windows, Linux, and more on your Mac, iPhone, and iPad. UTM is based on QEMU.

[Download macOS UTM QEMU](https://github.com/utmapp/UTM/releases/latest/download/UTM.dmg).


## Create VM

Launch UTM.


### Welcome

<img loading="lazy" src="/assets/images/screenshots/utm/step-1-welcome.png" alt="Screenshots / UTM / Step 1 Welcome">

* Choose "Create a New Virtual Machine".


### Start

<img loading="lazy" src="/assets/images/screenshots/utm/step-2-start.png" alt="Screenshots / UTM / Step 2 Start">

* Choose "Virtualize".


### Operating System

<img loading="lazy" src="/assets/images/screenshots/utm/step-3-operating-system.png" alt="Screenshots / UTM / Step 3 Operating System">

 * Choose the Custom area "Other".


### Other

<img loading="lazy" src="/assets/images/screenshots/utm/step-4-other.png" alt="Screenshots / UTM / Step 4 Other">

* Tap "Browse" then find file "OracleLinux-R8-U9-aarch64-dvd.iso".


### Hardware

<img loading="lazy" src="/assets/images/screenshots/utm/step-5-hardware.png" alt="Screenshots / UTM / Step 5 Hardware">
  
* Memory: 8192 (or whatever you prefer)

* CPU Cores: 2 (or whatever you prefer)


### Storage

<img loading="lazy" src="/assets/images/screenshots/utm/step-6-storage.png" alt="Screenshots / UTM / Step 6 Storage">

* 64 GB (or whatever you prefer)


### Shared Directory

<img loading="lazy" src="/assets/images/screenshots/utm/step-7-shared-directory.png" alt="Screenshots / UTM / Step 7 Shared Directory">

* Leave blank (or set it if you prefer)


### Summary

<img loading="lazy" src="/assets/images/screenshots/utm/step-8-summary.png" alt="Screenshots / UTM / Step 9 Summary">

* Click "Save".
  

### Play

<img loading="lazy" src="/assets/images/screenshots/utm/step-9-play.png" alt="Screenshots / UTM / Step 9 Play">

* Click the play icon.
  

### Install

<img loading="lazy" src="/assets/images/screenshots/utm/step-10-install.png" alt="Screenshots / UTM / Step 10 Install">

* Choose "Install Oracle Linux 8.9.0"


## Configure VM
        

### Install

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-01-install.png" alt="Screenshots / Oracle Linux setup / Step 1 Install">

Choose the language and locale:

* Choose English and United States (or whatever you prefer).


### Installation Summary

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-02-installation-summary.png" alt="Screenshots / Oracle Linux setup / Step 2 Installation Summary">

The next steps below will configure these:

1. Installation Destination

2. Network & Host Name

3. Create Root

4. Create User


### Installation Destination

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-03-installation-destination.png" alt="Screenshots / Oracle Linux setup / Step 3 Installation Destination">


### Network & Host Name

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-04-network-and-host-name.png" alt="Screenshots / Oracle Linux setup / Step 4 Network & Host Name">


### Create Root

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-05-root-password.png" alt="Screenshots / Oracle Linux setup / Step 4 Root Password">

Create root account:

* Check the box to create a root account. 

* Set the password to "changeme123XYZ!" (or whatever you prefer).

* Click "Done".


### Create User

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-06-create-user.png" alt="Screenshots / Oracle Linux setup / Step 6 Create User">

Create user account:

* Check the box to create a user account. 

* Set the username to "user" (or whatever you want). 

* Set the password to "changeme123XYZ!" (or whatever you prefer).

* Click "Done".


### Begin Installation

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-07-begin-installation.png" alt="Screenshots / Oracle Linux setup / Step 7 Begin Installation">

Eventually you should see a progress bar with the setup process.


### Installation Progress Copmlete

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-08-installation-progress-complete.png" alt="Screenshots / Oracle Linux setup / Step 8 Installation Progress Complete">

After the setup, you should see a message such as "Oracle Linux installation is successful". 

* Click the button "Reboot System".


## Eject & Reboot

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-09-reboot.png" alt="Screenshots / Oracle Linux setup / Step 9 Reboot">

You should see the Grub prompt with the Oracle Linux DVD ISO options.

* Eject the ISO by clicking the top right area icon that looks like a CD or DVD, with the tool tip "Drive image options".

* Type "c" to get a command prompt.

* Type `reboot` then press return.


## Initial Setup

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-10-initial-setup.png" alt="Screenshots / Oracle Linux setup / Step 10 Initial Setup">


## License Information

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-11-license-information.png" alt="Screenshots / Oracle Linux setup / Step 11 License Information">

After the reboot:

1. You should see a license choice. 

2. Accept the license.
   
3. Click "FINISH CONFIGURATION".


## License Accepted

<img loading="lazy" src="/assets/images/screenshots/oracle-linux-setup/step-12-license-accepted.png" alt="Screenshots / Oracle Linux setup / Step 12 License Accepted">


## Login

After the configuration:

1. You should see a typical Linux login screen.

2. Log in with username "user" and password "changeme123XYZ!" (or whatever you set up earlier).


### Welcome

<img loading="lazy" src="/assets/images/screenshots/user-setup/step-1-welcome.png" alt="Screenshots / User setup / Step 1 Welcome">


### Typing

<img loading="lazy" src="/assets/images/screenshots/user-setup/step-2-typing.png" alt="Screenshots / User setup / Step 2 Typing">


### Privacy

<img loading="lazy" src="/assets/images/screenshots/user-setup/step-3-privacy.png" alt="Screenshots / User setup / Step 3 Privacy">


### Ready To Go

<img loading="lazy" src="/assets/images/screenshots/user-setup/step-4-ready-to-go.png" alt="Screenshots / User setup / Step 4 Ready To Go">


### Getting Started

<img loading="lazy" src="/assets/images/screenshots/user-setup/step-5-getting-started.png" alt="Screenshots / User setup / Step 5 Getting Stated">


### Launch Terminal

<img loading="lazy" src="/assets/images/screenshots/user-setup/step-6-launch-terminal.png" alt="Screenshots / User setup / Step 6 Launch Terminal">


## Become root

Become root:

```sh
su
```


## Update

Update the operating system packages:

```sh
dnf --assumeyes update
dnf --assumeyes upgrade
dnf --assumeyes autoremove
```


## Install developer release package

Install the Oracle Linux developer release:

```sh
dnf install -y oraclelinux-developer-release-el8
```


## Choose database version

Search for the most-recent Oracle database preinstall package for aarch64:

```sh
dnf search oracle-database-preinstall | grep aarch64
```

As of 2024-01-01, the most-recent result is oracle-database-preinstall-19c.

Install:

```sh
dnf install -y oracle-database-preinstall-19c
```


## Download database

Oracle Database 19c for Aarch64 is not currently available via dnf. Instead, we download the database as a zip file.

In the VM, launch Firefox and browse:<br>
https://www.oracle.com/database/technologies/oracle-database-software-downloads.html#db_free

As of 2024-01-01, the most-recent result is `LINUX.ARM64_1919000_db_home.zip`.

Download it.

Move it to the conventional place:

```sh
mv LINUX.ARM64_1919000_db_home.zip /tmp/db_home.zip
```


## Make directories

Make directories, set ownerships, and set permissions as per Oracle Database 19c installation guide:

```sh
mkdir -p /u01/app/oracle
mkdir -p /u01/app/oraInventory
chown -R oracle:oinstall /u01/app/oracle
chown -R oracle:oinstall /u01/app/oraInventory
chmod -R 775 /u01/app
```


## Configure Oracle user

Set a password for the oracle user, so we can sign in later:

```sh
passwd oracle
```

Set the password to whatever you prefer.


## Oracle user

The installation process requires X11 and Xdisplay. 

The easiest way of making this work well is to become the correct user:

1. Sign out of the `root` user.

2. Sign in as the `oracle` user.

Run:

```sh
mkdir -p /u01/app/oracle/product/19.19/dbhome_1
cd /u01/app/oracle/product/19.0.0/dbhome_1
unzip /tmp/db_home.zip
./runInstaller
```

## TODO


Create network settings:

* Turn on Ethernet.

* Set host name to "host-name-example" (or whatever you prefer).

* Click "Done".



## Oracle Database 19c installer


### Step 1

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-1.png" alt="Screenshots / Oracle Database 19c installer / Step 1">


### Step 2

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-2.png" alt="Screenshots / Oracle Database 19c installer / Step 2">


### Step 3

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-3.png" alt="Screenshots / Oracle Database 19c installer / Step 3">


### Step 4

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-4.png" alt="Screenshots / Oracle Database 19c installer / Step 4">


### Step 5

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-5.png" alt="Screenshots / Oracle Database 19c installer / Step 5">


### Step 6

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-6.png" alt="Screenshots / Oracle Database 19c installer / Step 6">


### Step 7

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-7.png" alt="Screenshots / Oracle Database 19c installer / Step 7">


### Step 8

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-8.png" alt="Screenshots / Oracle Database 19c installer / Step 8">


### Step 9

<img loading="lazy" src="/assets/images/screenshots/oracle-database-19c-installer/step-9.png" alt="Screenshots / Oracle Database 19c installer / Step 9">

### Success

Oracle Database is now successfully installed.

To access it:<br>
https://localhost:5500/em
