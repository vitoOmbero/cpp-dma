cmake_minimum_required (VERSION 3.9)

project(client_lib)

add_compile_definitions(PTRS_ONLY)

add_library(${PROJECT_NAME} src/rescons.cpp)
add_library(sub::client ALIAS ${PROJECT_NAME})

target_link_libraries(${PROJECT_NAME} 
    sub::libload
)

target_include_directories(${PROJECT_NAME}
    PUBLIC    ${PROJECT_SOURCE_DIR}/include
)
