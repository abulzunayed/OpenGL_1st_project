cmake_minimum_required(VERSION 3.30.0)
project(hello_world VERSION 0.1.0 )

include(CTest)
enable_testing()

find_package(OpenGL REQUIRED)
add_executable(hello_world 
    src/config.h
    src/config.cpp 
    src/main.cpp  
    src/glad.c
    src/triangle_mesh.cpp
    src/triangle_mesh.h
    src/material.cpp
    src/material.h

    )

target_include_directories(hello_world PRIVATE dependencies)
target_link_libraries(hello_world glfw OpenGL::GL )