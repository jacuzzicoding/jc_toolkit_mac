cmake_minimum_required(VERSION 3.10) 
project(jctool)

#Specify The C++ standard
set(CMAKE_CXX_STANDARD 17)

#Add Executable
add_executable(jctool
    hid.c
    jctool.cpp
)

# Here is where we will include directories for header files
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

# Check if hidapi is found and link it
find_package(hidapi REQUIRED)
if(hidapi_FOUND)
    target_include_directories(jctool PRIVATE ${HIDAPI_INCLUDE_DIRS})
    target_link_libraries(jctool PRIVATE ${HIDAPI_LIBRARIES})
else()
    message(FATAL_ERROR "hidapi not found")
endif()