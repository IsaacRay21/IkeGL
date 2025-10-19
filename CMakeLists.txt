cmake_minimum_required(VERSION 3.15)
project(IkeGL LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# -------------------
# GLFW
# -------------------
include(FetchContent)

FetchContent_Declare(
    glfw
    GIT_REPOSITORY https://github.com/glfw/glfw.git
    GIT_TAG latest
)
FetchContent_MakeAvailable(glfw)

# -------------------
# GLAD
# -------------------
add_library(glad STATIC libs/glad/src/glad.c)
target_include_directories(glad PRIVATE libs/glad/include)

# -------------------
# Common include dirs
# -------------------
set(COMMON_INCLUDE
    libs/glad/include
    libs/glfw/include
    include
)

# -------------------
# Executables
# -------------------

# HelloTriangle
add_executable(HelloTriangle src/HelloTriangle/main.cpp)
target_include_directories(HelloTriangle PRIVATE ${COMMON_INCLUDE})
target_link_libraries(HelloTriangle PRIVATE glfw glad opengl32)


