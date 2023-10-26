# Aseprite TGA Library
# Copyright (C) 2020-2021  Igara Studio S.A.
cmake_minimum_required(VERSION 3.26)
project(tga)

# We need C++11 because we use the "override" keyword
set(CMAKE_CXX_STANDARD 11)

add_library(tga-lib
  decoder.cpp
  encoder.cpp
  image_iterator.cpp
  stdio.cpp)

set_target_properties(tga-lib PROPERTIES PUBLIC_HEADER "tga.h")
install(TARGETS tga-lib ARCHIVE DESTINATION lib PUBLIC_HEADER DESTINATION include)
