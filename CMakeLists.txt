cmake_minimum_required(VERSION 3.3)

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

project(test_regex)

add_subdirectory(libs)

add_executable(test_regex test.cpp)

target_link_libraries(test_regex boost::regex)
