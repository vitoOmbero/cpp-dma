cmake_minimum_required (VERSION 3.9)

project(resprov VERSION 1.0.0 DESCRIPTION "resprov provides SuperB matrices!!1")

add_library(${PROJECT_NAME} SHARED
    src/resprov.cpp
)

add_compile_definitions(EXTERN_C SUPERBMAT_DEBUG LIB_API_VER_1)

set_target_properties(${PROJECT_NAME} PROPERTIES 
    VERSION ${PROJECT_VERSION}
    SOVERSION 1
    PUBLIC_HEADER include/resprov/resprov.h
)

target_include_directories(${PROJECT_NAME}
    PRIVATE    ${PROJECT_SOURCE_DIR}/include
)

install(TARGETS ${PROJECT_NAME}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
    LIBRARY DESTINATION lib
)
