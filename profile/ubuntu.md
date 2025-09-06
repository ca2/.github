<!-- Installation -->
## Installation for Ubuntu


### Create directory

```bash
mkdir -p $HOME/code/operating_system
```

### Set up build environment
Clone tool-linux at code/operating_system folder
```bash
git clone https://github.com/ca2/tool-linux $HOME/code/operating_system/tool
cd $HOME/code/operating_system/tool/bin
./patch_shell
```
./patch_shell changes .bashrc and .profile. Please check and see if it is ok (always open to suggestions).

Reopen terminal to load extended PATH environment variable.

```bash
ubuntu_setup
# For Ubuntu
ubuntug4deps
# For Kubuntu
ubuntuk6deps
```

### Clone the project
```bash
git clone https://github.com/ca2/linux-simple $HOME/code/simple --recurse-submodules
```

### Run prepare_applications
```bash
cd $HOME/code/simple
checkout
prepare_applications
```

### Finally open a solution or Run CMake

```bash
# CLion
clion $HOME/code/simple/CMakeLists.txt
```

```bash
# CMake
cd $HOME/code/simple
mkdir cmake-build-debug
cd cmake-build-debug
cmake -S .. -B . -G Ninja
# for PC with 8 cores using 6 threads is fair enough -j 6
ninja -j 6 _app_simple_drawing
# to run _app_simple_drawing
output/_app_simple_drawing
```
