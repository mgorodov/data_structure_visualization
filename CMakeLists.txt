cmake_minimum_required(VERSION 3.21)
project(sfml_test)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXE_LINKER_FLAGS "-static -static-libgcc")
set(SFML_STATIC_LIBRARIES TRUE)

add_executable(sfml_test src/main.cpp)

set(SFML_DIR "C:\\SFML-2.5.1\\lib\\cmake\\SFML")

target_link_libraries(sfml_test sfml-graphics sfml-window sfml-system)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake_modules")
find_package(SFML COMPONENTS graphics window system REQUIRED)
