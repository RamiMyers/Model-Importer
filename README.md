# ModelImporter

ModelImporter is a small C++ / OpenGL program that loads Wavefront `.obj` models into GPU buffers and renders them using a minimal rendering pipeline. The project focuses on **data parsing**, **explicit memory management**, and **transformation hierarchies** (e.g., simulating orbital motion in a scene).

## Features
- Wavefront OBJ parsing (vertices / normals / indices)
- Explicit buffer construction and memory safety considerations (avoiding invalid writes / segfaults)
- Procedural geometry (sphere + torus used for the demo scene)
- Transform pipeline for relative motion (object rotation/orbit behavior)
- Matrix/vector math via **cglm**

## Requirements (Ubuntu)
- CMake
- A C++ compiler (g++ / clang++)
- OpenGL drivers
- **GLFW built from source and installed system-wide**
- **GLAD installed system-wide** (current setup; GLAD is not vendored in this repo)
- **cglm installed system-wide**

## Installing cglm (system-wide)
cglm provides a CMake-based build/install.

```bash
git clone https://github.com/recp/cglm.git
cd cglm
mkdir build && cd build
cmake ..
make
sudo make install
sudo ldconfig
## Building ModelImporter
From the repository root:
```

## Building ModelImporter
From the repository root:

```bash
mkdir build
cd build
cmake ..
make
```
