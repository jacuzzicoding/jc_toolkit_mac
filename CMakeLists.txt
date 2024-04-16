cmake_minimum_required(VERSION 3.10) 
project(jctool)
#The C++ standard
set(CMAKE_CXX_STANDARD 17)

add_executable(jctool jctool.cpp 

    hid.c
    jctool.cpp
    FormJoy.h
    Overrides.h
    hidapi.h
    hidapi_log.h
    ir_sensor.h
    jctool.h
    luts.h
    resource.h
    tune.h
)