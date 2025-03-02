cmake_minimum_required(VERSION 3.10)
project(Magma)

set(CMAKE_CXX_STANDARD 17)

# Includi il path del Vulkan SDK se necessario
find_package(Vulkan REQUIRED)

find_package(glfw3 REQUIRED)

add_executable(Magma src/main.cpp)
target_link_libraries(Magma Vulkan::Vulkan glfw)
