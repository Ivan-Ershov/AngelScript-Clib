cmake_minimum_required(VERSION 3.22)
project(clib)

add_subdirectory(../../../../AngelScript/sdk/angelscript/projects/cmake ./build)

add_compile_options(-c -fPIC)
add_link_options(-static)

add_library(clib STATIC ../../as_c.cpp)

target_include_directories(clib PRIVATE ../../angelscript_c.h)

target_link_libraries(clib PRIVATE angelscript)
