<!-- Installation -->
## Installation for Ubuntu


### Create directory

```bash
mkdir -p $HOME/cmake/operating_system
```

### Set up build environment
Clone tool-linux at cmake/operating_system folder
```bash
git clone https://github.com/ca2/tool-linux $HOME/cmake/operating_system/tool-linux
cd $HOME/cmake/operating_system/tool_linux/bin
./patch_shell
```
./patch_shell changes .bashrc and .profile. Please check and see if it is ok (always open to suggestions).

Reopen terminal to load extended PATH environment variable.

```bash
# For Ubuntu
ubuntudeps
# For Kubuntu
kubuntudeps
```

### Clone the project
```bash
git clone https://github.com/ca2/linux-simple-cmake $HOME/cmake/simple --recurse-submodules
```

### Install application_build_helper
```bash
cd
mkdir bin
cd bin
# For Ubuntu
wget https://ubuntu.ca2.store/24.04/application_build_helper
# For Kubuntu
wget https://kubuntu.ca2.store/24.04/application_build_helper
```

### Run prepare_applications
```bash
cd $HOME/cmake/simple
prepare_applications
```


### Finally open a solution

```bash
clion $HOME/cmake/simple/CMakeLists.txt
```
