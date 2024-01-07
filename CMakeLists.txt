cmake_minimum_required(VERSION 3.20)
project(Example)
add_executable(main main.cc)

find_package(Catch2 3 REQUIRED)
target_link_libraries(main PRIVATE Catch2::Catch2WithMain)
