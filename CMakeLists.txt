cmake_minimum_required(VERSION 3.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_FLAGS "-Werror")
set(CMAKE_CXX_FLAGS_DEBUG "-g")
set(CMAKE_CXX_FLAGS_RELEASE "-O3 -s -DNDEBUG")

project(dictionary-generator)

set(source src/main.cpp
		src/default.cpp
		src/generator.cpp
		src/files.cpp)
set(headers src/default.hpp
		src/generator.hpp
		src/files.hpp)

add_executable(dictionary-generator ${source} ${headers})
