cmake_minimum_required(VERSION 3.10)
project(MyApp)

set(CMAKE_CXX_STANDART 17)

add_subdirectory(glad)

include_directories(include)

add_executable(myapp main.cpp src/glad.c)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

target_link_libraries(myapp OpenGL::GL flw)
