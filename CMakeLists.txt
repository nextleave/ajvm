cmake_minimum_required(VERSION 3.9)
project(ajvm)
set(CMAKE_CXX_STANDARD 11)



add_library(mylib classloader.c interp_engine interp_engine.c vm_error vm_error.c trace trace.c libelf libelf.c safe_printf safe_printf.c log log.c slab.c garbage_collect.c)
add_executable(wvm wvm.c)
target_link_libraries(wvm mylib)