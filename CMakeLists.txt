cmake_minimum_required(VERSION 3.1)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake/")
include(ConfigureAllModules) 

project(tinyxml)

add_subdirectory(tinyxml)

__configure_all()