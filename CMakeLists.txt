cmake_minimum_required(VERSION 3.27.2 FATAL_ERROR)

set(PROJECT NAME 2Dgame-c++)
project(${PROJECT NAME})

add_executable(${PROJECT NAME} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT NAME} glfw)