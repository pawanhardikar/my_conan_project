cmake_minimum_required(VERSION 3.15)
project(MyConanZlibApp)

set(CMAKE_CXX_STANDARD 17)

# Include Conan toolchain config
include(${CMAKE_BINARY_DIR}/conan_toolchain.cmake OPTIONAL)

add_executable(my_app main.cpp)

# Find and link zlib (from Conan)
find_package(ZLIB REQUIRED)
target_link_libraries(my_app ZLIB::ZLIB)
