cmake_minimum_required(VERSION 3.3)

project(archemedies-engine)

add_executable(${PROJECT_NAME} src/Application.cpp)

add_subdirectory(external/glfw)

target_include_directories(${PROJECT_NAME}
        PUBLIC external/glfw/include
        PUBLIC external/glfw/deps/
        )

target_link_directories(${PROJECT_NAME}
        PUBLIC external/glfw/src
        PUBLIC external/glfw/deps/
        )

target_link_libraries(${PROJECT_NAME} glfw)
