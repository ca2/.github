## Installation for Windows

### code.exe

Instead of doing steps described below, you can download and run [https://windows.ca2.store/code.exe](https://windows.ca2.store/code.exe).

### Unicode UTF-8 for worldwide language support
In this framework, some variables are named using unicode characters. In order to compile you must set this feature on your windows machine.
Download and run [https://windows.ca2.store/utf8.reg](https://windows.ca2.store/utf8.reg) and restart machine.

### tool-windows
At Git Bash
```bash
cd /c/
mkdir operating_system
git clone https://github.com/ca2/tool-windows C:\operating_system\tool-windows --recurse-submodules
```

### Add C:\operating_system\tool-windows\bin and C:\operating_system\bin to the `PATH` environment variable
1. Press the windows key so you can search
2. Type environment variables and click on `Edit the system environment variables`
3. Add the bottom of the window, click `Environment Variables...`
4. In the top list, scroll and search for the `PATH` environment variable. Double click it.
5. On the right, click `New`
6. Enter the path `C:\operating_system\tool-windows\bin` then press enter.
7. Click `New` again.
8. Enter the path `C:\operating_system\bin` then press enter.
9. Done!

### application_build_helper
Download [https://windows.ca2.store/application_build_helper.exe](https://windows.ca2.store/application_build_helper.exe) to `C:\operating_system\bin\application_build_helper.exe`.
This path is accessible from systems `PATH`, making life easier.
```bash
wget https://windows.ca2.store/application_build_helper.exe -O /c/operating_system/bin
```

### storage-windows
Unzip [https://windows.ca2.store/storage-windows.zip](https://windows.ca2.store/storage-windows.zip) to `C:\operating_system\storage-windows`.

### Clone simple project
Suggested name of folder is simple.
```bash
git clone https://github.com/ca2/windows-simple-solution /c/simple --recurse-submodules
```

### Symbolic links will be broken, so...

### Enable Developer Mode for Windows at Developer Settings

### Install Tortoise Git

### delete folder C:\simple\port\include

### Revert C:\simple\port\include deletion using Tortoise Git by right clicking at C:\simple\port

Open `C:\simple\solution-windows\simple.sln` project you can now build and run ca2 simple solution.



