cmake_minimum_required(VERSION 2.8)
project(7bit-portal)

# set some project-wide flags
set( CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -Wno-overflow" )

set( LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/lib/pc CACHE PATH
        "Single Directory for all Libraries")

# all source files
file(GLOB_RECURSE SRC src/*.cpp)

set( CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fpermissive" )

# compile portal itself
add_executable(7bit-portal ${SRC})
