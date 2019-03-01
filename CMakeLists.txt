cmake_minimum_required(VERSION 3.11)
project(SMPL+H)

set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV REQUIRED)

set(SOURCE_FILES main.cpp posemapper.h lbs.h)
add_executable(SMPL+H ${SOURCE_FILES})

include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(SMPL+H ${OpenCV_LIBS})