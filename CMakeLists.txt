cmake_minimum_required(VERSION 3.20)

project(bj VERSION 0.1.0 LANGUAGES CXX)

add_executable(bj src/main.cpp)

target_compile_features(bj PRIVATE cxx_std_20)

if(MSVC)
    target_compile_options(bj PRIVATE /W4 /permissive-)

else()
    target_compile_options(bj PRIVATE
    -Wall
    -Wextra
    -Wpedantic
    -Wconversion
    -Wshadow
    )
endif()