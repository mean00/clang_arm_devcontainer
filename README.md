This is a simple devcontainer setup to build the arm-toolchain project for embedded
( https://github.com/arm/arm-toolchain )

The main goal is to easily get a cortexM toolchain fully working inside a devcontainer based
on ubuntu 24.04

By default it will pull HEAD, but you can just checkout the version you want in the arm-toolchain folder

# Howto :

  git submodule update --init
  devpod up . --ide none --devcontainer-path .devcontainer/devcontainer.json
  mkdir build
  cd build
  cmake ..
  make -j 8
  make toolchain
  make package-llvm-toolchain
