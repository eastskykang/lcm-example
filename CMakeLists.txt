cmake_minimum_required(VERSION 3.11)

project(lcm-example)

find_package(lcm REQUIRED SYSTEM)

add_subdirectory(lcm)
add_subdirectory(src)