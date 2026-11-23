## Installation for Windows

```diff
# code.exe (Currently not working)
# Instead of doing steps described below, you would be able to download and run [https://windows.ca2.store/code.exe](https://windows.ca2.store/code.exe).
# Currently it is not working. I need to work on it.
```

### Install Git-SCM
Download and install the proper version of Git for your windows:
* https://git-scm.com/install/windows
  
It is important to check the option to "Enable Symbolic Links" when installing Git-SCM.

It is in the last Tab of Options of the Installation Wizard.

### Configure Git symbolic links
At Git Bash
```bash
git config --global core.symlinks true
```

### Enable Developer Settings at Windows
Go to Windows Settings > Developer Settings and enable the first toggle button and it is good idea also to click the Apply buttons (with respective check boxes selected).

### Unicode UTF-8 for worldwide language support
ca2 platform uses variable names that may have Unicode characters in it. In order to compile such source you must set option in Windows that enable proper handling of UTF-8 data.
1. Access the link [https://raw.githubusercontent.com/ca2/tool-windows/refs/heads/main/registry/utf8.reg](https://raw.githubusercontent.com/ca2/tool-windows/refs/heads/main/registry/utf8.reg)
2. Right click the file in the browser and save the file as utf8.reg somewhere in PC.
3. Double click the downloaded utf8.reg file to run it.
4. Restart machine to apply Settings.
   
You may need to manually rename the .txt extension from .reg.txt to .reg (Windows File Explorer may be configured to hide known file extensions like .txt. You may at *File Explorer Options* > *View tab*, uncheck the option: "Hide extensions for known file types". One of check boxes of Developer Options in Apply buttons would enable this option).

### Clone "windows-simple" solution: a solution with a couple of "simple" applications
Suggested name of folder is windows-simple/windows-simple.

At Git bash.
```bash
git clone --recurse-submodules --branch latest_release https://github.com/ca2/windows-simple $HOME/code/windows-simple/windows-simple
```

If symbolic links are broken, please take a look at this: [windows-repair-git-symlinks.md](windows-repair-git-symlinks.md)

### Open "simple" solution at Visual Studio

* Install Visual Studio 2026.
At Visual Studio Installer, select `Desktop Development with C++`
  
[https://visualstudio.microsoft.com/](https://visualstudio.microsoft.com/)
  
* Open `%USERPROFILE%\code\windows-simple\windows-simple\solution-windows\simple.sln` project.

### Set "shared_app_simple_drawing" as Startup Project

* Right click the project "_app_simple_drawing" at "Solution Explorer" and click option "Set as Startup Project"
* Click the play button to Run the _app_simple_drawing project

It will build the platform and the application and then run it.



