## Installation for Windows

### code.exe

Instead of doing steps described below, you can download and run [https://windows.ca2.store/code.exe](https://windows.ca2.store/code.exe).

### Unicode UTF-8 for worldwide language support
In this framework, some variables are named using unicode characters in source code. In order to compile such source code you must set this feature on the windows machine where you are going to setup this ca2 Software Development Environment.
Download and run [https://windows.ca2.store/utf8.reg](https://windows.ca2.store/utf8.reg) and restart machine.

### tool-windows
At Git Bash
```bash
cd
mkdir code
cd code
mkdir operating_system
cd operating_system
git clone https://github.com/ca2/tool-windows $HOME/code/operating_system/tool --recurse-submodules
```

### Add C:\Users\<username>\code\operating_system\bin and C:\Users\<username>\code\operating_system\tool\bin to the `PATH` environment variable
1. Press the windows key so you can search
2. Type environment variables and click on `Edit the system Environment Variables`
3. At the top list, select *Path* list item, then click `Edit...`
4. On the right, click `New`
5. Enter the path `%USERPROFILE%\code\operating_system\bin` then press Enter.
6. Click `New` again.
7. Enter the path `%USERPROFILE%\code\operating_system\tool\bin` then press Enter.
8. Done!

### storage-windows
Unzip [https://windows.ca2.store/storage-windows.zip](https://windows.ca2.store/storage-windows.zip) to `C:\Users\<username>\code\operating_system\storage-windows`.

### Clone simple project
Suggested name of folder is simple.
```bash
git clone https://github.com/ca2/windows-simple-solution $HOME/code/simple --recurse-submodules
```

### Symbolic links will be broken, so...

### Enable Developer Mode for Windows at Developer Settings

### Install Tortoise Git

### delete folder C:\Users\<username>\code\simple\port\include

### Revert C:\simple\port\include deletion using Tortoise Git by right clicking C:\Users\<username>\code\simple\port and clicking Revert option in Context Menu Tortoise Git Sub Menu

### At Tortoise Git Revert Screen, select everything and then click Revert.

Open `C:\Users\<username>\code\simple\solution-windows\simple.sln` project you can now build and run ca2 simple solution.



