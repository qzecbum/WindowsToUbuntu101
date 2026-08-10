# *Full guide* to switch from **Windows** to **Ubuntu** in a Day

## Table of Contents
- [Info](#info)
- [1. Package Manager](#1-package-manager)
- [2. Desktop Environments](#2-desktop-environments)
- [3. Kde Plasma](#3-kde-plasma)
- [4. Setting up Flathub](#4-setting-up-flathub)
- [5. Installing Google Chrome](#5-installing-google-chrome)
- [6 Keeping Your System Updated](#6-keeping-your-system-updated)
- [7. Microsoft Applications](#7-microsoft-applications)
- [8. WinApps Setup](#8-winapps-setup)

## Info
- Install ubuntu 24.04 normally, nothing special just normal, then reboot into it.
## 1. Package Manager
*In this section we will talk about using the APT package manager*

1. Once you are in the desktop, go ahead and open the terminal app, you should see a terminal on your screen
2. Next, you will learn how to use the ``apt`` package manager, this is where you will learn how to update and upgrade your system. 
3. Go ahead and update your package repos, which will update the package list, aka a list for where to get the packages from. 
4. You can update the pacakge list with the following command ``sudo apt update``. Tip, if it fails yo umight not be connected to internet.
5. You will see the end of the terminal output stating that ``x packages can be upgraded`` this means it succesfully fetched the packages. 
6. You will now update the packages, run the command ``sudo apt upgrade`` to install the packages that have an update. Think of this as a windows update but no restart required.
7. Your packages should all be upgrading to the latest version. You will know when you are done once you see your name again at the botton. 

## 2. Desktop Environments
*In this section we will talk about desktop environments or a DE*

- When you talk about Linux, you are talking about a **just a terminal**, but this is a *overloaded* version of linux. **Plain *vanilla* Linux is just a terminal**, no apps, no software, nothing. **So how do you have an amazing user interface right at your hands**?
- This magic is done by a tool called a **desktop**. You are using a *flavor* of linux called Ubuntu, which comes with a desktop called **gnome**, which is what your are using righjt now
- **Can I switch desktops?** Yes, on any linux flavor **you can shoose any desktop**, you just need to install them with your package manager.
- In this guide you will be using the **KDE Plasma** which is a very stable desktop which a familiar **windows like UI**.

## 3. Kde Plasma
*This section is about setting up and using KDE Plasma*

### 3.1 Installation
1. With your terminal still open install the package, ``kde-plasma-desktop``. To do this, you will need to use the command ``sudo apt install kde-plasma-desktop``. 
2. After it loads the package it will ask you *Do you want to continue?* This is where you will press the **Y** key and then enter to accept of the installation
3. It will then download and install the package and its dependencies. 
4. When you see the screen called **CONFIGURING SDDM** move to the next part of the guide to understand this concept.

### 3.2 Display Managers
- To understand a **display manager is**, you need to understand then *vanilla* linux **is only a terminal**, no ui or anything. So when you boot into your system, The **Graphical User Interface** that greets you to select your user and login to your desktop is a Display Manager.
- The one you used is called ``GDM`` or **Gnome Display Manager**. This is the default login manager, which manages your logins and security.

### 3.3 Choosing the Display Manager
1. Press **OK** on the screen that gives you information.
2. It will then ask you to select which display manager you want to use. ``GDM`` is recomended **for security and simplicity to use**, it might show up as ``gdm3`` **select it with your arrow keys and click** ``enter``.
3. **The installation will continue**.

### 3.4 Entering KDE Plasma
- **Please wait until the installation of KDE Plasma** is complete before moving on, **you will know by seeing your name in the bottom of the terminal output.**
1. Once you have finshed installing KDE, **you can now switch desktops into it**. In gnome, press the **wifi and sound icon in the top right corner to see your controls**
2. You will see the Power menu on the top right corner, select it.
3. Then press the logout button, and confirm the logout.
4. You will now be back in the **GDM Display Manager**. Select the user, **but dont sign in yet**.
5. Select the **Gear Icon** in the bottom right corner, and select **Plasma** *or Plasma-X11*
6. Once selected, **you may sign in**.

### 3.5 KDE Plasma (High DPI Issue)
- *This section shows you how to fix the ui if everything looks tiny, **You can skip this step if it looks fine***.
#### 3.5.0 High DPI Issue
- On some **high resolution displays**, you may have a very small desktop, This is becuase KDE *Fails* to detect the correct display scaling.
1. Open the **KDE Menu**, similar to the Windows Start Button, And yo ushould see the System Settings icon as a pinned app, **Open it**
2. On the left side panel, Scrolldown until yo ufind the **Hardware** Section
3. Inside this section, select the **Display and Monitor** sub section.
4. Find the **Global Scale** and slide it up to 150% or 200%, depending on your display, then select **Apply**.
5. Finally **reboot your computer** for all the changes to **apply**.
6. If your Taskbar still looks small, **right click** an empty on the taskbarthen select **Enter Edit Mode**. 
7. Bump up the **Panel Height Slider** until it looks good, then press the ``ESC`` key twice to leave the edit mode.

## 4. Setting up Flathub
*This section will teach you how to use flathub to et more applications*
### 4.1 What is Flathub?
- **Flathub** is a **host** of **Application** that are *extremly simple to install and setup*. Once it is setup, you will be able to *access* more **software** that the ``APT`` Package Manager simply **doesnt have the rights to access**.

### 4.2 How Flathub Works
- **Flathub** and **Flatpak** are to different things, **Flatpak** is the **engine**, and lets say **Flathub** is the place where all the **apps are stored**, or a **repository**. 

### 4.3 Installing Flatpak (The engine)
1. Since you are in the **KDE Plasma** desktop, you can open your terminal with the **default keybinding**, ``ctrl + alt + t`` . 
2. In the terminal you can simply install the flatpak engine with the following command ``sudo apt install flatpak``.
3. Type ``y`` and click ``enter``

### 4.4 Installing Flathub (The repo)
1. *Flatpak* is **nothing** without a repository, which lets **flatpak** know where the apps are **stored**.  
2. To install the **Flathub** repository, you can use the following command, ``flatpak remote-add flathub https://dl.flathub.org/repo/flathub.flatpakrepo``

#### 4.4.1 Breaking Down the Command
``flatpak remote-add flathub https://dl.flathub.org/repo/flathub.flatpakrepo``
- ``flatpak``: **calling** the flatpak engine.
- ``remote-add``: telling **flatpak** to **add a repository**
- ``flathub``: the **name** of the repository
- ``url``: the **url** of the repo

## 5. Installing Google Chrome
*This section will help you **install Google Chrome** and help you understand **Open Source Software** and **Closed Source Software**.

### 5.1 Open Source vs. Closed Source
- There are two types of mainstream software. This cna include **Open Source** and **Closed Source**. 
- **Open Source Software** is when the developer make the software free and availble to the public, meaning *anyone* can **access and view** the code, making it the **Safest option**.
- **Closed Source or Proprietary Software** is a privatly owned software where you cant view the code. and cannot be **viewed** or **optimized** by the community
- The ``APT`` Package Manager only lets you download **Open Source Software**, Meaning you cant install chrome.

### 5.2 Installing Chrome
1. The best way to get **closed source** software is through **Flathub**: Open your **browser** and go to ``flathub.org``
2.  Once you are there, **search** for ``Google Chrome``
3. Select the one by **google**, and **DONT click on the install button**
4. **Instead** click on the **Arrow** next to the install button.
5. Here you will see two commands, the **Install** command and the **Run** command.
6. Since you are on KDE, **you only need the first command**, go ahead and **copy it**.
7. Open your terminal with ``ctrl + alt + t`` and paste in the command with ``ctrl + shift + v`` . **Click enter**.
8. Click ``enter`` when it asks you to install it.
9. Click ``enter`` again to **accept** the changes to the system.

## 6 Keeping Your System Updated
*This section will help you keep your system updated and secured*

### 6.1 Updating Open Source Applications
- Updating your **opensource applications** is done via the ``APT`` Package Manager. This only require two commands. 
- The first command is to load the package lists, aka where to get each package from, and is the following, ``sudo apt update``
- The second command is to actually **install** the packages it found that **require updating**, ``sudo apt upgrade``.  

### 6.2 Updating Closed Source Applications
- Updating closed source application is **more important**, as they contain security fixes and patches that are **required** to stay safe. 
- To do this, it only requires one command, ``flatpak update``

### 6.3 Updating Frequency
- Both types of package updates should be updated **within short time periods**, this could be once a week, and at **least once a month**, it should become a habit so you can **stay safe**.

## 7. Microsoft Applications
*This section will explain compatibilty with the Microsoft Application Suite*

### 7.1 How it Works
- **Some** microsoft apps such as ``Microsoft Edge`` and ``Microsoft Teams`` can be installed through **flathub** and **work great!**
- **Other apps** such as the **Microsoft Office Suite** need *extra tuning* to work, but can still be done.
- To do this, we can use a tool called WinApps.

### 7.2 What is WinApps?
- WinApps is a community built tool that lets you **create a windows computer, inside of your existing computer**, then mirror the apps back to your desktop, **making them feel like native**.

#### Everything after this is **optional**, This can take up to **1 Hour** depending on your hardware, and you **Cannot** stop in between

#### Most of the work takes only 15 minutes, but you will need to keep the computer on for the rest of the time for windows setup.

## 8. WinApps Setup
*This section is about installing and setting up WinApps on Ubuntu*

#### Settings up WinApps
- Open your favorite webbrowser and search ``WinApps``, click on the first link by ``winapps-org`` . 
- This is a **Github repo**, where the **code** for WinApps is **stored**.
- The first step is to install **Docker.** 

#### Installing Docker
- To install docker type in ```sudo apt install docker.io docker-compose-v2``` and let it run
- Add yourself in docker with ``sudo usermod -aG docker $USER``
- Add yourself in KVM with ``sudo usermod -aG kvm $USER``
- verify that it worked with ``docker compose version``, then restart your computer with ``sudo reboot``.

#### Install Dependencies for WinApps
- Open your web browser and go to the same WinApps github
- From there, scroll down to the ``Installation`` section and at ``Step 2: Install Dependencies``. 
- Copy the required command for **debian/ubuntu** and paste it in your terminal with ``ctrl + shift + v``.
- While still in your terminal, you need to make a folder at ``~/.config/winapps/``, you cna make it with the following command: ``mkdir .config/winapps``

#### WinApps Configuration
- Now you can change your current directory to this new folder with the command ``cd .config/winapps``
- Once you are in the **right directory,** go back to the **Github repo and scroll down to** ``Step 3``. 
- Copy the big text block with the **copy icon in the corner.**
- Now **open the config file** in a text editor with ``kate winapps.conf`` and **Paste the whole file inside of it**. 
- But before you save, press ``ctrl + f`` and search for ``AUTOPAUSE`` (line 123) and change it to ``on``.
- And also find ``RDP_TIMEOUT`` (line 159) and change it to 60
- Then press ``ctrl + s`` and close the window.

#### Docker Configuration
- Go back to the GitHub and scroll all the way up where you see the files and folders
- find the file names ``compose.yaml`` and select it.
- in the top right corner select the **copy button** (beside the raw button).
- Open your terminal and **verify you are in the** **right directory by the blue text.**
- use kate to open it ``kate compose.yaml``
- Paste it in the file, **but dont save yet.**

#### File Configuration (compose.yaml)
- Go to **line 20**, and change the **disk** size to ``32G``
- Go to **line 18**, and change the **ram** size to ``2G``
- go to **line 17**, and change the **version** to ``tiny11``
- **Now save the file and close Kate**


#### Starting the Docker Engine
- Back in your terminal, run the command, ``docker compose up``
- It will download the image and do everything for you.
- This process will **Take some time**, Plug in your laptop and click on the battery symbol on the tray
- At the top of the popup, check the symbol that says ``Manually block sleep and screen locking``
- **Dont leave the laptop until the output "downloading tiny11 from archive" changes, then you can leave** 
- **To check the windows installation progress, you can go to** ``127.0.0.1:8006`` in your browser.


**Set a timer for about like 40 to 50 minutes depending on your internet speed, and then check back**

#### Setting up  the Docker VM
- **After some time** open a browser and go to ``127.0.0.1:8006`` and verify that your **windows desktop is visible**, once it is **you can close the tab**.
- After closing the tab, wait **1 minute** for the connection to close.
- Then, open your terminal and press the ``new tab``  button in the top right corner of the terminal to use terminal again.
- Go back to the WinApps github page, use ``ctrl + f`` to search for ``Step 5``.

#### Winapps Configuration Wizard.
- In the window use arrow keys and the enter key to interact
- In the blue windows that opened, select ``Install``
- Next select ``Current User``
- Now select ``Manual``
- **WAIT until a Window pops up, select the ``ok`` button on the windows sign in screen**.

#### Second Blue Menu
- It will asks you ``handling official supported applications``
- From this on, click ``enter`` for every other question.

#### Finishing Setup
- After your terminal says ``INSTALLATION COMPLETE`` in green text **do the following instructions**.
- Enable docker on boot ``sudo systemctl enable docker``
- Finally, **Restart your Computer**, ``sudo reboot``.

**Your WinApps is Successfully installed!**
#### Installing Applications
- **To install an Windows application**, open the app named ``Windows`` in your KDE menu then install the apps that you would install on Windows.
- To add it as an app on your desktop, type this command in your terminal, ``winapps-setup`` 
- Select ``Install``
- Select ``System``
- Select ``Manual``
- *You made need to type your password*
#### Accessing Local Files
- To open local files, **open the folder called** ``shared`` **on your desktop**, there you can see your files from your REAL ubuntu machine.
#### Known Issues
- After a reboot, you must wait 1 - 2 minutes before opening a windows application
- Multy tasking windows applications can be a bit clunky

