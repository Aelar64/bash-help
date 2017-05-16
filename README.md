### Before Use
**_Make sure you are in Windows 10 Anniversary Update!_**

*Enabling the program*
______________________
To enable the program on the computer, you must go to your settings and enable Development Mode. Then, you need to go to the control panel, click Programs, then click Turn Windows features on or off. Find Windows Subsystem for Linux and enable it. Restart your computer, then log in.
1. Open Settings
2. Enable Developer Mode
3. Close settings (optional) and open Control Panel.
4. Click Programs
5. Click Turn Windows features on or off
6. Find Windows Subsystem for Linux (Beta)
7. Turn it on
8. Hit OK then restart your computer.

Create a shortcut on your desktop. In the target box, set it to `C:\Windows\System32\bash.exe ~ --login`. Run the program.  
Your Linux root directory can be found at `C:\Users\<username>\AppData\Local\lxss\rootfs`.
To change your home directory, type the following commands into Command Prompt (Admin):
```batch
lxrun /setdefaultuser root
bash
```
```shell
sudo usermod -d <directory> <user>
exit
```
```batch
lxrun /setdefaultuser <user>
```
Your C drive can be found at `/mnt/c`.  
You can change `.profile` at `C:\Users\<username>\AppData\Local\lxss\home\<Terminal name>\.profile` if you didn't change your home directory or `~/.profile`, where `~` is your home directory.  
If the colors aren't working properly when you type `ls`, put this into `.profile`:
```shell
alias ls='ls --color=auto'
```
To run `java-install.sh`, navigate the the folder where you downloaded the JDK, then run the program. The JDK can be found [here](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).
