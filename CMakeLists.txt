cmake_minimum_required(VERSION 3.30)
project(OpenGL_Project)

set(CMAKE_CXX_STANDARD 20)

# Find OpenGL
find_package(OpenGL REQUIRED)

# Add GLFW
find_package(glfw3 REQUIRED)
include_directories(/opt/homebrew/include)

#Add GLEW
find_library(GLEW_LIB glew REQUIRED)
include_directories(/opt/homebrew/include)

# Add Executable
add_executable(OpenGL_Project main.cpp)

# Link Libraries
target_link_libraries(OpenGL_Project OpenGL::GL glfw ${GLEW_LIB})
