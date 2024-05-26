cmake_minimum_required(VERSION 3.15)

project(ari_final VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Set the vcpkg toolchain file
set(CMAKE_TOOLCHAIN_FILE "${CMAKE_CURRENT_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake" CACHE STRING "Vcpkg toolchain file")

# Find Boost program_options
find_package(Boost REQUIRED COMPONENTS program_options)
include_directories(vcpkg)

# Add the executable
add_executable(ari_final src/main.cpp)

# Link Boost program_options
target_link_libraries(ari_final PRIVATE Boost::program_options)
