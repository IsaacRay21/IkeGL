# IkeGL

IkeGL is a personal OpenGL project following the LearnOpenGL tutorials. Its purpose is to serve as both a learning tool and a foundation for a future custom graphics engine.


## Build Instructions

This project uses CMake and is designed for Windows with Visual Studio 2022.

1. Create a build directory:
 ```bash
mkdir build
cd build
```

2. Run CMake to configure:
```bash
cmake -G "Visual Studio 17 2022" -A x64 ..
```
3. Build the project from Visual Studio or using:
```bash
cmake --build .
```

The executable will be generated in the build folder.

## Libraries

- **GLFW**: Used for window creation, input handling, and context management.  
- **GLAD**: OpenGL function loader, generated to match LearnOpenGL requirements.

## Progress Tracking

- [x] Getting Started
    - [x] Creating a window
    - [x] GLAD initialization
    - [x] Viewport setup
    - [ ] Hello Triangle
- [ ] Shaders
    - [ ] Shader class
    - [ ] Compiling and linking shaders
    - [ ] Using multiple shaders
- [ ] Textures
    - [ ] Loading textures
    - [ ] Using textures in shaders
    - [ ] Texture wrapping and filtering
- [ ] Transformations
    - [ ] Model, view, projection matrices
    - [ ] Translation, rotation, scaling
    - [ ] Coordinate systems
- [ ] Lighting
    - [ ] Basic lighting (ambient, diffuse, specular)
    - [ ] Phong lighting
    - [ ] Material properties
- [ ] Advanced Lighting
    - [ ] Multiple lights
    - [ ] Lighting maps (diffuse, specular)
    - [ ] Gamma correction
- [ ] Camera
    - [ ] Camera class
    - [ ] Free movement
    - [ ] View and projection matrices
- [ ] Model Loading
    - [ ] Assimp integration
    - [ ] Loading .obj or other formats
    - [ ] Rendering models

