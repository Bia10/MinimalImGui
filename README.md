## Introduction

Minimal GUI example project using ImGui, OpenGL 3.0 and CMake.

![ImGui Example Screenshot](images/minimalimgui.png)

* [imgui](https://github.com/ocornut/imgui) - Minimal GUI.
* [glad](https://github.com/Dav1dde/glad) - OpenGL Function Loader.
* [glfw](https://github.com/glfw/glfw) - Windowing and Input.

## Using ImGui in a CMake Project 

To use the ImGui in a CMake project one should copy the following files:

* `3rdparty/imgui` - directory with ImGui headers copied from the original repository. This is not a git module, so the files are not updated automatically.
* `cmake/imgui.cmake` - CMake module that defines variables `IMGUI_LIBRARIES` and `IMGUI_INCLUDE_DIR`.

## Environment Setup

### Debian-based Systems

The following instructions apply to:

* Ubuntu 18.04
* Ubuntu 16.04
* Debian 9

```
sudo apt-get install -y \
    build-essential \
    cmake \
    xorg-dev \
    libgl1-mesa-dev \
    libfreetype6-dev
```

## Building

Check out sources with `--recursive` parameter for 3rd-party libraries:

```
git clone --recursive https://github.com/Postrediori/MinimalImGui.git
```

Prepare build with CMake and build executable

```
cd MinimalImGui
mkdir build && cd build
cmake ..
make
make install
```

## Running

Using `make install` will copy the executable to `bundle/MinimalImGui` directory:

```
cd build
make install
```

Run the binary from `bundle/MinimalImGui`:

```
cd bundle/MinimalImGui
./MinimalImGui
```

