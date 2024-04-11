cmake_minimum_required(VERSION 3.22)
project(test)

add_subdirectory(../../../projects/cmake ./build)

add_compile_options(-c -fPIC)
add_link_options(-static)

add_executable(test ../../source/main.c)

target_link_libraries(test PRIVATE clib)
