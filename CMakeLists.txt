cmake_minimum_required(VERSION 3.28)
project(CMakeSFMLProject LANGUAGES CXX)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
option(BUILD_SHARED_LIBS "Build shared libraries" OFF)

find_package(SFML COMPONENTS system window graphics)

set(CMAKE_CXX_STANDARD 17)

add_executable(main src/main.cpp)
target_link_libraries(main PRIVATE sfml-graphics)