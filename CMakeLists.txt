#
# note that,
# MSVC should not use this build system due to libpng stuff.
#
# in-tree build may not work due to dirent name collision.
#

cmake_minimum_required(VERSION 4.2.0)

project(kgtools LANGUAGES CXX)

set(CMAKE_POLICY_VERSION_MINIMUM 3.5)
add_subdirectory(external/libpng EXCLUDE_FROM_ALL)

add_executable(kg_pack
  kg_pack/kg_pack.cpp)
target_include_directories(kg_pack PRIVATE
  external/libpng)
target_link_libraries(kg_pack PRIVATE
  png_static)

add_executable(kg_depack
  kg_unpack/kg_unpack.cpp)
target_include_directories(kg_depack PRIVATE
  external/libpng)
target_link_libraries(kg_depack PRIVATE
  png_static)

install(TARGETS
  kg_pack
  kg_depack)
