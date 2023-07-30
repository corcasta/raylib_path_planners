cmake_minimum_required(VERSION 3.0.0)
project(PathPlanners VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

add_executable(PathPlanners src/main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

find_package(raylib REQUIRED)
include_directories(${raylib_INCLUDE_DIRS})
target_link_libraries(PathPlanners ${raylib_LIBRATIES})