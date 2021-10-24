cmake_minimum_required(VERSION 3.0.0)
project(densemesh VERSION 1.0.0)

include(CTest)
enable_testing()

aux_source_directory(./src SRC_LIST)
add_executable(densemesh ${SRC_LIST})

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

find_package(Eigen3 REQUIRED)

include_directories(${EIGEN3_INCLUDE_DIRS})
