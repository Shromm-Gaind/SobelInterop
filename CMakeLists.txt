cmake_minimum_required(VERSION 3.1 FATAL_ERROR)
project(SobelInterop VERSION 1.0)
set(CMAKE_CXX_STANDARD 20)

set(OpenGL_GL_PREFERENCE GLVND)

find_package(OpenCL REQUIRED)
find_package(OpenCV REQUIRED)
find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

add_executable(SobelInterop main.cpp)
target_link_libraries(SobelInterop ${OpenCL_LIBRARIES} ${OpenCV_LIBS} ${OPENGL_LIBRARIES} glfw)