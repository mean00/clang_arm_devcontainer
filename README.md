This is a simple devcontainer setup to build the arm-toolchain project for embedded
( https://github.com/arm/arm-toolchain )

The main goal is to easily get a cortexM toolchain fully working inside a devcontainer based
on ubuntu 24.04

By default it will pull clang+picolibc v21.1.8, but you can just checkout the version you want in the arm-toolchain folder

# Howto :

```bash
git submodule update --init
devpod up . --ide none --devcontainer-path .devcontainer/devcontainer.json
ssh llvmarmdevcontainer.devpod
mkdir build
cd build
cmake -G Ninja ..
ninja package-llvm-toolchain
```
