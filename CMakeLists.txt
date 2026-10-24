cmake_minimum_required(VERSION 3.16)
project(hello_gl CXX C)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

# glad is generated into ./glad (see README steps)
add_library(glad STATIC glad/src/gl.c)
target_include_directories(glad PUBLIC glad/include)

add_executable(app main.cpp)
target_link_libraries(app PRIVATE glad glfw OpenGL::GL ${CMAKE_DL_LIBS})
