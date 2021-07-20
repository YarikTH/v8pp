cmake_minimum_required(VERSION 3.14)

project(v8pp LANGUAGES CXX)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}")

# On Ubuntu 20.04 install package libnode-dev because libv8-dev is redirected there
find_package(V8)

# TODO: add warning flags setup
# TODO: add option to skip tests targets

add_subdirectory(v8pp)
add_subdirectory(test)
add_subdirectory(plugins)
