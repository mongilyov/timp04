cmake_minimum_required(VERSION 3.24)
project(hwApp)

add_executable(${PROJECT_NAME} sources/hello_world.cpp)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/include)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib formatter_ex)

target_link_libraries(${PROJECT_NAME} formatter_ex)
