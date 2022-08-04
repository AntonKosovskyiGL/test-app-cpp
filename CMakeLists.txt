cmake_minimum_required(VERSION 3.17...3.23)
get_filename_component(CMAKE_TOOLCHAIN_FILE "extern/vcpkg/scripts/buildsystems/vcpkg.cmake" REALPATH)
project(test-app LANGUAGES CXX)

find_package(Catch2 CONFIG REQUIRED)
find_package(spdlog CONFIG REQUIRED)

add_executable(app src/main.cpp)
target_compile_features(app PRIVATE cxx_std_17)
