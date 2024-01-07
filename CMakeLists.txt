cmake_minimum_required(VERSION 3.20)
project(Example)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
add_executable(main main.cc)

find_package(Catch2 3 REQUIRED)
target_link_libraries(main PRIVATE Catch2::Catch2WithMain)
