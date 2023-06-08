# Todo

cmake_minimum_required(VERSION 3.20)
 
if ("${CMAKE_BINARY_DIR}" STREQUAL "${CMAKE_SOURCE_DIR}")
  message(FATAL_ERROR "No In-source builds!
    Please create a subfolder, cd into it and use `cmake ..` inside it.
    If it doesn't exist `mkdir build` will create a directory called build.
    You can use the build folder or create a folder with any name, have fun!
    NOTE: The command you just ran creates CMakeCache.txt and the folder CMakeFiles.
    Unfortunately because you ran the command inside the wrong folder, they are in the wrong place!
    You gotta remove them, or cmake will refuse to work. 
    Don't worry, this isn't a big deal, cmake is a real pain to work with sometimes.")
endif()

project(CamGrab VERSION 0.6.9 LANGUAGES CXX)

if(MSVC)
    set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS TRUE)
    set(BUILD_SHARED_LIBS TRUE)
    add_compile_options(/W3)
else()
    add_compile_options(-Wall -Wextra)
endif()

add_subdirectory(src)

# add_executable(CamGrab src/main.cpp)
