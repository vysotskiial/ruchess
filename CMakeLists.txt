cmake_minimum_required(VERSION 3.1)
project(ruchess VERSION 1.0)

find_package(Qt5 REQUIRED COMPONENTS Widgets)
find_package(GTest REQUIRED)

set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_AUTOUIC ON)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Wshadow")
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(IMAGES_INSTALLATION_PATH "${CMAKE_INSTALL_PREFIX}/share/draw_cpp")

add_executable(ruchess src/main.cpp)
target_link_libraries(ruchess Qt5::Widgets)
