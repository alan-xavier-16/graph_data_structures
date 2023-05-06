# Define cmake version
cmake_minimum_required(VERSION 3.19)

# Project name
project(graphds 
  VERSION 1.0 
  DESCRIPTION "Graph Data Structures in C++" 
  LANGUAGES CXX)

# Set C++ standard
set(CMAKE_CXX_STANDARD 20)

# Set compiler options
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++20 -Wall -Wextra -Wpedantic")

# Define Target
add_executable(graphds
  src/main.cpp
  src/Node.h
  src/Node.cpp
  )