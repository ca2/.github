## Installation for Windows

### code.exe

[https://windows.ca2.store/code.exe](https://git-scm.com/](https://windows.ca2.store/code.exe) will do all following steps.

### Dependencies

This framework requires a couple dependencies to build, this section will go through how to install them.
You will need [git](https://git-scm.com/) to be able to follow along.

### Installation Location
You can install the dependencies anywhere, but they must be added to the systems `PATH` environment variable.
The following example will show you how to install them in the `C:\CA2FrameworkDependencies` folder.

### Create the directory for the Dependencies
```bash
cd C:\
mkdir CA2FrameworkDependencies
cd CA2FrameworkDependencies
mkdir tool-windows
```
### Downloading the dependencies
They are located inside [this](https://github.com/ca2/tool-windows) repository. They are things generally required for the build system or the application itself.
```bash
git clone https://github.com/ca2/tool-windows C:\CA2FrameworkDependencies\tool-windows --recurse-submodules
```
### Adding them to the `PATH` environment variable
There should be a directory under `C:\CA2FrameworkDependencies\tool-windows` called `bin`. You should add this to your systems environment variables. 

#### How to add to `PATH`
1. Press the windows key so you can search
2. Type environment variables and click on `Edit the system environment variables`
3. Add the bottom of the window, click `Environment Variables...`
4. In the top list, scroll and search for the `PATH` environment variable. Double click it.
5. On the right, click `New`
6. Enter the path `C:\CA2FrameworkDependencies\tool-windows\bin` (**or your chosen directory**) then press enter.
7. Done!

### The build helper tool
You can download the build helper tool from [here](https://windows.ca2.store/application_build_helper.exe)
After downloading this file, move it to the path `C:\CA2FrameworkDependencies\tool-windows\bin`. It lives here because we already set this path in the systems `PATH`, so it makes life easier.

#### If you're using WSL, here is a bash script to do this automatically

```bash
wget https://windows.ca2.store/application_build_helper.exe -O /mnt/c/CA2FrameworkDependencies/tool-windows/bin
```

### Other dependencies
These dependencies must be inside `C:\Users\YourUserName\operating_system`. This is because *CA2* projects directly depend on library's inside of this directory.

You can create this directory like this inside of the command prompt. Don't forget to replace `YourUserName` with whatever your username is.
```bash
cd C:\Users\YourUserName
mkdir operating_system
```

### Clone the project
As it stands, `storage-windows` cannot be downloaded fast. It's on my home server and I don't have great upload speeds.

`storage-windows.zip` contains **port** projects, pre-built binaries and things like OpenSSL and ffmpeg binaries.

You can build "port" projects by checking out https://github.com/ca2/windows-simple-solution and building the solution file ./solution-windows/port.sln .

We now need to install these dependencies, *below* are links to each. We recommend you download `storage-windows-x64.zip`. This is what I use most. These are needed for building in `x64`.

1. [x64 Binaries](https://windows.ca2.store/storage-windows-x64.zip) (**RECOMMENDED**) But Only x64
2. [x64 Static Binaries](https://windows.ca2.store/storage-windows-x64-static.zip)
3. [x32 Binaries](https://windows.ca2.store/storage-windows-Win32.zip)
4. [x32 Static Binaries](https://windows.ca2.store/storage-windows-Win32-static.zip)
5. [All Binaries](https://windows.ca2.store/storage-windows.zip)

### What to do with `storage-windows-*.zip`
This is where the directory we created under `C:\Users\YourUserName\operating_system` come in.
Within that directory, create a folder called `storage-windows`. Then, extract the contents of the `.zip` file into that directory.

*for reference*: The folder inside of `storage-windows` will be just `x64` or `x32` if you've done this correctly.

```bash
mkdir -p C:/operating_system/bin
wget https://windows.ca2.store/application_build_helper.exe -O /c/operating_system/bin/application_build_helper.exe
```

### Clone the windows project
We recommend that you install it under `C:\Users\YourUserName\simple`. This isn't required, but is suggested.

**This example shows how to clone the suggested way**
```bash
git clone https://github.com/ca2/windows-simple-solution C:\Users\YourUserName\simple --recurse-submodules
# dont forget to replace "YourUserName"!
```

### Building the ports
Once you've cloned the windows project, follow these steps for `Visual Studio`.

Inside of the **simple** directory, there should be a folder called `solution-windows`, navigate into it. Then, open `port.sln`. Once the project is open, click on `Build` at the top and click `Build Solution`.

Once that is done, close that project and open the other project `simple.sln`. 

### Almost there
In this framework, some variables are named using unicode characters, so in order to compile you must set a feature on your windows machine.
1. Press the windows keys and search `Control Panel`, click the first application.
2. Once open, select `Clock and Region`
3. Select `Region`
4. In the new window, select the `Administrative` tab.
5. Press `Change system locale`
6. Check `Beta: use Unicode UTF-8 for worldwide language support`
7. Done!

Your finished, with your `simple.sln` project you can now build and run CA2 framework!

