cmake_minimum_required(VERSION 4.3)
project(snake C)

set(CMAKE_C_STANDARD 23)

list(APPEND CMAKE_PREFIX_PATH "/opt/homebrew")
find_package(SDL3 REQUIRED)

add_executable(snake main.c)

target_link_libraries(${PROJECT_NAME} PRIVATE SDL3::SDL3)
target_include_directories(${PROJECT_NAME} PRIVATE ${SDL_INCLUDE_DIRS})
