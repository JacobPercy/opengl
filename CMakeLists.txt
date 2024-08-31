cmake_minimum_required(VERSION 3.4...3.28)
project(OpenGLProject CXX)

# Specify the path to GLFW
set(GLFW_DIR "${CMAKE_SOURCE_DIR}/libs/GLFW")

# Specify the C++ standard (e.g., C++11, C++14, C++17)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add GLFW include and lib directories
include_directories(${GLFW_DIR}/include)
link_directories(${GLFW_DIR}/lib)

# Add the executable
add_executable(OpenGLProject src/test.cpp)

# Link GLFW
target_link_libraries(OpenGLProject glfw3)

# Optionally, you can also set the target properties, such as linking with other libraries
# target_link_libraries(OpenGLProject glfw3 ${OPENGL_LIBRARIES})
