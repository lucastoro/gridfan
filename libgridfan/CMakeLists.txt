cmake_minimum_required(VERSION 3.1.3)
project(libgridfan)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON) 
set(CMAKE_CXX_EXTENSIONS OFF)

add_library(${PROJECT_NAME} SHARED libgridfan.cpp serial.c)
target_link_libraries(${PROJECT_NAME} ${LIBSENSORS})
install(TARGETS ${PROJECT_NAME} LIBRARY DESTINATION lib)
