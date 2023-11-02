cmake_minimum_required(VERSION 3.16)

project(openFrameworks
  VERSION 0.12.0
  LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(libs)
add_subdirectory(addons)
