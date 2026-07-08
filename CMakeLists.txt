cmake_minimum_required(VERSION 3.8)
project(raytracing LANGUAGES C CXX)

add_executable(
    raytracing 
    # It's recommended to list all .cpp files explicitly as opposed to using
    # glob syntax
    main.cxx
)

# Set your C++ standard to C++20
target_compile_features(raytracing PUBLIC cxx_std_20)
