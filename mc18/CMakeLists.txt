cmake_minimum_required(VERSION 3.10)
project(MinecraftOS)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(SDL2 REQUIRED)
find_package(OpenGL REQUIRED)

include_directories(${SDL2_INCLUDE_DIRS})
link_directories(${SDL2_LIBRARY_DIRS})

add_executable(minecraftos
    src/main.cpp
)

target_link_libraries(minecraftos
    ${SDL2_LIBRARIES}
    GLESv2
)
