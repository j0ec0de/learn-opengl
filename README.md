# OpenGL Projects

A small C++17 OpenGL 3.3 core-profile project using GLFW for windowing and GLAD for loading OpenGL functions. It opens an 800x600 window and clears it to a solid color. Press `Esc` to quit.

## Requirements

- CMake 3.16+
- A C++17 compiler
- GLFW 3 (e.g. `sudo apt install libglfw3-dev`)
- OpenGL development libraries (e.g. `sudo apt install libgl1-mesa-dev`)

GLAD is already included in `glad/`.

## Build and run

```bash
cmake -B build
cmake --build build
./build/app
```

## Project layout

- `main.cpp`: window setup and render loop
- `CMakeLists.txt`: build configuration
- `glad/`: generated GLAD OpenGL loader (`include/` and `src/`)
