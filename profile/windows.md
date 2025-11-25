## Installation for Windows

### code.exe (Currently not working)

Instead of doing steps described below, you would be able to download and run [https://windows.ca2.store/code.exe](https://windows.ca2.store/code.exe).
Currently it is not working. I need to work on it.

### Install Git-SCM
Download and install the proper version of Git for your windows:
* https://git-scm.com/install/windows 
It is important to check the option to "Enable Symbolic Links" when installing Git-SCM. It is in the last Options Screen of the Installation Wizard.

### Configure Git symbolic links
At Git Bash
```bash
git config --global core.symlinks true
```

### Enable Developer Settings at Windows
Go to Windows Settings > Developer Settings and enable the first toggle button and it is good idea also to click the Apply buttons (with respective check boxes selected).

### Unicode UTF-8 for worldwide language support
This framework uses variables that may have Unicode characters. In order to compile such source you must set option in Windows that enable proper handling of UTF-8 data.
1. Access the link [https://raw.githubusercontent.com/ca2/tool-windows/refs/heads/main/registry/utf8.reg](https://raw.githubusercontent.com/ca2/tool-windows/refs/heads/main/registry/utf8.reg)
2. Right click the file in the browser and save the file as utf8.reg somewhere in PC.
3. Double click the downloaded utf8.reg file to run it.
4. Restart machine to apply Settings.
   
You may need to manually rename the .txt extension from .reg.txt to .reg (Windows File Explorer may be configured to hide known file extensions like .txt. You may at *File Explorer Options* > *View tab*, uncheck the option: "Hide extensions for known file types". One of check boxes of Developer Options in Apply buttons would enable this option).

### Clone tool-windows
At Git Bash
```bash
cd
mkdir code
cd code
mkdir operating_system
cd operating_system
git clone https://github.com/ca2/tool-windows $HOME/code/operating_system/tool --recurse-submodules
```

### Update PATH environment variable
1. Press the windows key so you can search
2. Type "Environment Variables" and click on `Edit the system environment variables` to open `System Properties` dialog.
3. Click `Environment Variables...` button at bottom of screen to open `Environment Variables` dialog.
4. At the list at the top, select *Path* list item, then click `Edit...` to open `Edit environment variable` dialog.
5. On the right, click `New`
6. Enter the path `%USERPROFILE%\code\operating_system\bin` then press Enter.
7. Click `New` again.
8. Enter the path `%USERPROFILE%\code\operating_system\tool\bin` then press Enter.
9. Click Ok at `Edit environment variable` dialog.
10. Click Ok at `Environment Variables` dialog.
11. Click Ok at `System Properties` dialog.
12. Done!

### Download and uncompress storage-windows
Unzip [https://ca2.network/download/storage/storage-windows.zip](https://ca2.network/download/storage/storage-windows.zip) to `C:\Users\<username>\code\operating_system\storage-windows`.

### Clone simple project
Suggested name of folder is simple.

At Git bash.
```bash
git clone https://github.com/ca2/windows-simple $HOME/code/simple --recurse-submodules
```

### Symbolic links will be broken, so...

1. Enable Developer Mode for Windows at Developer Settings (If you havent't done so yet).
2. Install Tortoise Git
3. Delete folder %USERPROFILE%\code\simple\port\include
4. Revert %USERPROFILE%\code\simple\port\include deletion using Tortoise Git by right clicking %USERPROFILE%\code\simple\port and clicking Revert option in Context Menu Tortoise Git Sub Menu

### At Tortoise Git Revert Screen, select everything and then click Revert.

Open `%USERPROFILE%\code\simple\port\include` project you can now build and run ca2 simple solution.



