cmake_minimum_required(VERSION 2.8)

project (AE)

set(EXECUTABLE_OUTPUT_PATH ${AE_SOURCE_DIR}/bin/${CMAKE_BUILD_TYPE})
set(LIBRARY_OUTPUT_PATH ${AE_SOURCE_DIR}/lib)

if (CMAKE_COMPILER_IS_GNUCXX)
    message(STATUS "GNUCXX compiler")
    set (CMAKE_CXX_FLAGS "-Wall -Wextra -lpthread -g")
endif ()

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

add_subdirectory(${AE_SOURCE_DIR}/src)
