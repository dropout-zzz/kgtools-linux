cmake_minimum_required(VERSION 4.2.0)

project(kgtools LANGUAGES CXX)

add_executable(kg_pack
  kg_pack/kg_pack.cpp)

add_executable(kg_depack
  kg_unpack/kg_unpack.cpp)
