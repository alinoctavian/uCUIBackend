cmake_minimum_required(VERSION 3.7)

project(UCUIBackend)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} CMakeModules/)

set(PROJ_NAME UCUIBackend)
set(SRC_DIR src)
set(INCLUDE_DIR include)

include_directories(${EXECUTABLE}
    ${INCLUDE_DIR}/*
    ${CMAKE_CURRENT_SOURCE_DIR}
)

file(GLOB SRC_FILES 
    ${SRC_DIR}/*
)

add_library(${PROJ_NAME} STATIC ${SRC_FILES})