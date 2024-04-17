cmake_minimum_required(VERSION 3.13)  # CMake version check
project(poco-test)               # Create project
set(CMAKE_CXX_STANDARD 14)            # Enable c++14 standard

find_package(Poco REQUIRED Foundation Net JSON)

include_directories(${Poco_INCLUDE_DIRS})

# Add .cpp file of the project root directory as a source file
set(SOURCE_FILES poco-test.cpp)

# Add executable target with source files listed in SOURCE_FILES variable
add_executable(poco-test ${SOURCE_FILES})

target_link_libraries(poco-test ${Poco_LIBRARIES})


