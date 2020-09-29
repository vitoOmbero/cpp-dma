cmake_minimum_required (VERSION 3.9)

project(foreignlib_load)

add_library(${PROJECT_NAME} INTERFACE)
add_library(sub::libload ALIAS ${PROJECT_NAME})

target_include_directories(${PROJECT_NAME}
    INTERFACE
        ${PROJECT_SOURCE_DIR}/include
        ${PROJECT_SOURCE_DIR}/../shared_lib/include
)
