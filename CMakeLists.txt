include(FetchContent)
cmake_minimum_required(VERSION 3.17)

project(learningopengl LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

FetchContent_Declare(
        imgui-glfw-glad-glm
        GIT_REPOSITORY https://github.com/cmmw/imgui-glfw-glad-glm.git
)

FetchContent_MakeAvailable(imgui-glfw-glad-glm)

add_executable(app main.cpp)

target_link_libraries(
        app
        imgui
        glm
)
