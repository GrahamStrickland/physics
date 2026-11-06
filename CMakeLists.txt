cmake_minimum_required(VERSION 3.24)
project(physics
    VERSION 0.0.1
    DESCRIPTION "Numerical solutions and plots for exercises from \"Introduction to Classical Mechanics\" - David Morin"
    HOMEPAGE_URL "https://github/com/GrahamStrickland/physics"
    LANGUAGES CXX
)

set(CMAKE_EXPORT_COMPILE_COMMANDS on)
set(CMAKE_CXX_STANDARD 26)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g -std=c++26 -pedantic -Wall -Wextra -Werror")

set(SOURCES
    src/utils.cpp
    src/p1_7.cpp
    src/ex1_17.cpp
    src/ex1_18.cpp
    src/main.cpp
)

add_executable(physics ${SOURCES})

target_compile_features(physics PUBLIC cxx_std_26)

target_include_directories(physics PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
