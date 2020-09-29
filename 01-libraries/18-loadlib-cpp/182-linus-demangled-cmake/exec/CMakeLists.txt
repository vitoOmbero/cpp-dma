cmake_minimum_required (VERSION 3.9)

project(test.out)

add_executable(${PROJECT_NAME} main.cpp)

# add_compile_definitions(PTRS_ONLY)

set (LDFLAGS "-Wl,-rpath,.")

target_link_libraries(${PROJECT_NAME}
    sub::libload
    sub::client 
    dl
    ${LDFLAGS}
)

install(
  TARGETS ${PROJECT_NAME}
  RUNTIME DESTINATION bin
  LIBRARY DESTINATION lib
)
