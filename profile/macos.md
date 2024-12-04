<!-- Installation -->
# $${\color{red}Attention! : Draft}$$

## Installation for macOS

### Create directory

```bash
mkdir -p $HOME/workspace/operating_system
```

### Set up build environment
Clone tool-macos at workspace/operating_system folder
```bash
git clone https://github.com/ca2/tool-macos $HOME/workspace/operating_system/tool-macos
cd $HOME/workspace/operating_system/tool-macos/bin
./patch_shell
```
./patch_shell changes .zhrc and .profile. Please check and see if it is ok (always open to suggestions).

Reopen terminal to load extended PATH environment variable.

### Clone the project
```bash
git clone https://github.com/ca2/macos-simple-workspace $HOME/workspace/simple --recurse-submodules
```

### Run prepare_applications
```bash
cd $HOME/workspace/simple
checkout
prepare_applications
```


### Finally open a solution or Run CMake

```bash
# Xcode
open $HOME/workspace/simple/simple.xcworkspace
```


