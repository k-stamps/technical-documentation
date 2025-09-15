## Getting Started with Windows Subsystem for Linux (WSL) and VS Code

WSL (Windows Subsystem for Linux) makes it possible to run a Linux distribution on Windows.

Note: When using WSL, you can either point to your files in mnt (your Windows file system) or in home (the Linux home directory). For better performance, it's advised to use the Linux home directory, which is what these directions use.

Instructions for setting up WSL with an Ubuntu installation and using it in VS Code:

### Ensure the WSL capability is turned on:
In Windows, search for “Features” and select “Turn Windows features on or off”
In the “Windows Features” dialog box make sure the "Windows for Linux Subsystem” option is selected, and Save.
Also, make sure the “Virtual Machine Platform” option is also selected, and Save.
Close the “Windows Features” dialog and restart the computer.

### Install the latest version of WSL:
* Open a Command Prompt window as Administrator (search Windows for “Command Prompt” and select “Run as Administrator.”
* In the Command Prompt, enter:

```
> wsl --update
```
It will update to the newest version, displaying the version it is updating to.

When WSL 2 is installed in the previous step the popular Ubuntu linux distribution by default. If prompted, add a Unix username and password of your choosing. Restart the computer.

To see a list of possible WSL commands:
```
> wsl --help
```
To see what distro of linux you are now running:
```
> wsl -l -v
```

### Ubuntu shell:
* To open the Ubuntu shell, search Windows for “Ubuntu”
* To see your files in Ubuntu:
```
$ wsl
```
* To see your files using Windows Explorer, look at the icons in the bottom left of the Explorer. Insight Linux is Ubuntu. Select Ubuntu, then the home folder. In the home folder will be a folder with your Ubuntu username. Inside that folder is where your Ubuntu home directory is. In the explorer search window, it will display as:

\\wsl.localhost\Ubuntu\home\[username]

* To open the current location from the Ubuntu terminal in windows explorer:
*```
$ explorer.exe .
```
The dot means current directory.

* To navigate to the home dir in Ubuntu:
```
$ cd ~
```
(the tilde symbol is shorthand for the user’s home directory)

* To open a folder in VS code
```
$ code .
```

To start Ubuntu in VS code:
Click the lower left blue tab and select WSL. The blue tab will then say “WSL: Ubuntu”

Resources: 
* https://learn.microsoft.com/en-us/windows/wsl/install 
* https://www.linkedin.com/learning/learning-windows-subsystem-for-linux-16134127 