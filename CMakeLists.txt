cmake_minimum_required(VERSION 4.1)
project(godot_online_subsystem)

set(CMAKE_CXX_STANDARD 20)

add_library(godot_online_subsystem SHARED src/library.cpp)
