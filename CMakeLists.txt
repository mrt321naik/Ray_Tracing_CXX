cmake_minimum_required(VERSION 4.1) # Adjusted version
project(raytracing LANGUAGES C CXX)

add_executable(
    raytracing 
    # It's recommended to list all .cpp files explicitly as opposed to using glob syntax
    src/main.cc
    includes/color.h
    includes/vec3.h
    includes/ray.h
    includes/hittable.h
    includes/sphere.h
    includes/hittable_list.h
    includes/rtweeked.h
    includes/interval.h
    includes/camera.h
)

# 1. No commas
# 2. Add a scope (PRIVATE)
# 3. Point to the folder, not the individual files
target_include_directories(raytracing
    PRIVATE 
    ${CMAKE_CURRENT_SOURCE_DIR}/includes 
)

# Set your C++ standard to C++20
# (Changed to PRIVATE since an executable doesn't expose its features to other targets)
target_compile_features(raytracing PRIVATE cxx_std_20)