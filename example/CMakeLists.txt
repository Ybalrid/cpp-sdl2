cmake_minimum_required(VERSION 2.8)
project(cpp-sdl2-example)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ./cmake-modules)
find_package(SDL2 REQUIRED)
find_package(Vulkan REQUIRED)

include_directories(../sources/ )


add_executable(example main.cpp)
target_link_libraries(example SDL2::SDL2 Vulkan::Vulkan)

