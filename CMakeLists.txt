cmake_minimum_required(3.15)

project("clearProject" VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)

target_link_libraries(${PROJECT_NAME} PUBLIC)

include_directories(includes)
add_library(${PROJECT_NAME} SHARED)
target_sources(${PROJECT_NAME} PRIVATE source/main.cpp)

set_target_properties(${PROJECT_NAME} PROPERTIES OUTPUT_NAME ${PROJECT_NAME SUFFIX ".dll")
