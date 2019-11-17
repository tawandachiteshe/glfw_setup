cmake_minimum_required(VERSION 3.14)
project(glfwTest)

set(CMAKE_CXX_STANDARD 14)
find_package (OpenGL REQUIRED)
include_directories("C:/GLFW/include")
link_directories("C:/GLFW/lib-mingw-w64")
#find_package (glfw3 REQUIRED)

set(SOURCE_FILES main.cpp)
add_executable(glfwTest ${SOURCE_FILES})
target_link_libraries (glfwTest ${OPENGL_LIBRARIES} glfw3 glu32 opengl32)