cmake_minimum_required(VERSION 3.16)

project(mjtest 
    VERSION 0.1
    LANGUAGES CXX)

add_executable(main main.cpp)
target_include_directories(main PUBLIC
    include
    extern/include)

target_link_directories(main PUBLIC 
    extern)

target_link_libraries(main PUBLIC
    mujoco
    glfw)