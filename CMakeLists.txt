cmake_minimum_required(VERSION 3.10) 
project(jctool)
set(CMAKE_CXX_STANDARD 17)

add_executable(jctool jctool.cpp hid.c)
