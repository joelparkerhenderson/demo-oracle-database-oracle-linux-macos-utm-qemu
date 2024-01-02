# Demo Oracle Database + Oracle Linux + macOS UTM QEMU

Demonstration of:

* Oracle Database 19c Aarch64

* Oracle Linux 8 Aarch64

* macOS UTM QEMU emulator

Feedback welcome.


## Download Oracle Linux

Oracle Linux 8 Aarch64 DVD ISO is a full installation disk image. It can work with system emulators and virtual machine hosts.

[Download Oracle Linux 8 Aarch64 DVD ISO](https://yum.oracle.com/ISOS/OracleLinux/OL8/u9/x86_64/OracleLinux-R8-U9-x86_64-dvd.iso).


## Download macOS UTM QEMU

UTM is a user-friendly full-featured system emulator and virtual machine host for iOS and macOS. UTM enables you to run Windows, Linux, and more on your Mac, iPhone, and iPad. UTM is based on QEMU.

[Download macOS UTM QEMU](https://github.com/utmapp/UTM/releases/latest/download/UTM.dmg)


## Create VM

Launch UTM and choose to create a new VM.

Steps:

1. "Start" dialog:

  * Choose "Virtualize".

2. "Operating System" dialog: 

   * Choose the Custom area "Other".

3. "Other" dialog:

  * Tap "Browse" then find file "OracleLinux-R8-U9-aarch64-dvd.iso".
  
  * Memory: 8192 (or whatever you prefer)

  * CPU Cores: 1 (or whatever you prefer)

4. "Storage" dialog:

  * 64 GB (or whatever you prefer)
  
5. "Shared Directory" dialog:

  * As is.


## Configure VM

Choose the language:

* We choose English.

Create root account:

* Check the box to create a root account. 

* Set the password to "changethispassword" (or whatever you prefer).

* Click "Done".

Create user account:

* Check the box to create a user account. 

* Set the username to "user" (or whatever you want). 

* Set the password to "changethispassword" (or whatever you prefer).

* Click "Done".

Create network settings:

* Turn on Ethernet.

* Set host name to "host-name-example" (or whatever you prefer).

* Click "Done".

Eventually you should see a progress bar with the setup process.

After the setup, you should see a message such as "Oracle Linux installation is successful". 

Click the button "Reboot System".


## Reboot VM

After the VM is created:

1. If the VM reboots, then you might see the Grub prompt with the Oracle Linux DVD ISO options.

2. Eject the ISO by clicking the top right area icon that looks like a CD or DVD, with the tool tip "Drive image options".

3. Type "c" to get a command prompt. Type `reboot` then press return.
   

## Accept license

After the reboot:

1. You should see a license choice. 

2. Accept the license.
   
3. Click "FINISH CONFIGURATION".


## Login

After the configuration:

1. You should see a typical Linux login screen.

2. Log in with username "user" and password "changethispassword" (or whatever you set up earlier).
   
3. Launch a terminal.

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

Become root:

```sh
su
```

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
