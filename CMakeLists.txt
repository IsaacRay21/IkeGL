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
# Create executable
# -------------------
add_executable(${PROJECT_NAME}
    src/main.cpp
    libs/glad/src/glad.c       # <- use your local path
)

# Include directories
target_include_directories(${PROJECT_NAME} PRIVATE
    libs/glad/include
    libs/glfw/include
)

# Link libraries
target_link_libraries(${PROJECT_NAME} PRIVATE
    glfw
    opengl32
)
