cmake_minimum_required(VERSION 3.20)

# # use homebrew installed llvm
# set(llvm_dir /opt/homebrew/opt/llvm)
# set(CMAKE_C_COMPILER ${llvm_dir}/bin/clang)
# set(CMAKE_CXX_COMPILER ${llvm_dir}/bin/clang++)
# link_directories(${llvm_dir}/lib)
# include_directories(${llvm_dir}/include)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
add_compile_options(-Wall -Wextra -Wpedantic)

project(main)
find_package(Catch2 3 REQUIRED)

link_libraries(Catch2::Catch2WithMain)

add_executable(main main.cc)
