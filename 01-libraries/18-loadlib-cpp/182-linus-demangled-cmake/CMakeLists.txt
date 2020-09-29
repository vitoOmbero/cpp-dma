cmake_minimum_required (VERSION 3.9)

project("test.out")

set (CMAKE_INSTALL_PREFIX "./") 
set (CMAKE_INSTALL_INCLUDEDIR "./inc")

set(CMAKE_VERBOSE_MAKEFILE ON)
set(CMAKE_INSTALL_RPATH "${CMAKE_INSTALL_PREFIX}/lib")
set(CMAKE_INSTALL_RPATH_USE_LINK_PATH TRUE)

add_subdirectory(loadhelp_ho_lib)
add_subdirectory(client_lib)
add_subdirectory(exec)
add_subdirectory(shared_lib)

