cmake_minimum_required(VERSION 3.10)
project(calculator)

set(CMAKE_CXX_STANDARD 11)

add_library(calculator STATIC calculator.cpp)
add_executable(calculator_app main.cpp)
target_link_libraries(calculator_app calculator)
