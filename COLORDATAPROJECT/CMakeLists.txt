# Minimum version of CMake required
cmake_minimum_required(VERSION 3.10)

# Project name
project(colordatareader VERSION 1.0 LANGUAGES CXX)

# C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Source files
set(SOURCES
    source.cpp
    imgui/imgui.cpp
    imgui/imgui_demo.cpp
    imgui/imgui_draw.cpp
    imgui/imgui_tables.cpp
    imgui/imgui_widgets.cpp
    imgui/imgui_impl_glfw.cpp
    imgui/imgui_impl_opengl3.cpp
)

# Include directories
include_directories(
    ${PROJECT_SOURCE_DIR}/include
    ${PROJECT_SOURCE_DIR}/include/GLFW
    ${PROJECT_SOURCE_DIR}/include/glm
    ${PROJECT_SOURCE_DIR}/include/KHR
    ${PROJECT_SOURCE_DIR}/imgui
)

# Add the GLAD library
add_subdirectory(vendor/glad)

# Add executable
add_executable(colordatareader ${SOURCES})

# Link libraries
target_link_libraries(colordatareader PRIVATE glad ${PROJECT_SOURCE_DIR}/libs/glfw3.lib)

file(COPY ${PROJECT_SOURCE_DIR}/CIEXYZ1931DATA.csv DESTINATION ${CMAKE_BINARY_DIR})

# Build types
set(CMAKE_BUILD_TYPE Debug)

