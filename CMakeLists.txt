# CMake Version
cmake_minimum_required(VERSION 3.11.3)

# CXX Standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED true)

# Project name
project(PathFinding)

# Add the path of the cmake files to the CMAKE_MODULE_PATH
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake)

# Set library output path to /lib
set(LIBRARY_OUTPUT_PATH "${CMAKE_SOURCE_DIR}/out/lib")

# Locate libraries in system
find_package(io2d REQUIRED)
find_package(Cairo)
find_package(GraphicsMagick)

# Add 3rdparty: pugixml and googletest
add_subdirectory(3rdparty/pugixml)
add_subdirectory(3rdparty/googletest)

# Add project executable
file(GLOB SOURCES src/*cpp)
add_executable(${PROJECT_NAME} ${SOURCES})

# Link libraries
target_link_libraries(${PROJECT_NAME}
    PRIVATE io2d::io2d
    PUBLIC pugixml
)