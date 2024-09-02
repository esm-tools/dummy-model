cmake_minimum_required(VERSION 3.10)

# set the project name
project(HelloWorld)

# specify the Fortran compiler
enable_language(Fortran)

# Set the install prefix to be in the repo tree, not in /
set(CMAKE_INSTALL_PREFIX ${CMAKE_SOURCE_DIR})

# specify where the binary files should be placed
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

# specify where the source files are located
file(GLOB SOURCES "src/*.f90")

# add the executable
add_executable(HelloWorld ${SOURCES})

# add the install targets
install(TARGETS HelloWorld DESTINATION bin)
