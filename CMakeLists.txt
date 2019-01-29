cmake_minimum_required(VERSION 3.9)
project(ixy VERSION 1.0.0)

set(CMAKE_C_STANDARD 11)

add_compile_options(-g -O2 -march=native -fomit-frame-pointer -std=c11
  -Wall
  -Wextra
  -Wno-unused-parameter
  -Wno-unused-function
  -Wformat=2
  )

add_subdirectory(src)
