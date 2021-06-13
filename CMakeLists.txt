cmake_minimum_required(VERSION 3.13)  # CMake version check
project(Maze)               # Create project "simple_example"
set(CMAKE_CXX_STANDARD 14)            # Enable c++14 standard

# Add main.cpp file of project root directory as source file



SOURCE_GROUP (visualization REGULAR_EXPRESSION src/visualization/.*) 

set(SOURCE_FILES

src/visualization/grid.h
src/visualization/grid.cpp

)



# Add executable target with source files listed in SOURCE_FILES variable
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src)

add_executable( maze main_maze.cpp ${SOURCE_FILES})



