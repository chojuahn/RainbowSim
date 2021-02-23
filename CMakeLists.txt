cmake_minimum_required(VERSION 3.4)
set_property(GLOBAL PROPERTY USE_FOLDERS ON)

# Set the target name - this should happen before almost anything becuase it
# causes CMake to detect things like the compiler and set various variables
project(RainbowSim)

set(CMAKE_LIBRARY_OUTPUT_DIRECTORY
	${PROJECT_BINARY_DIR}/bin)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY
	${PROJECT_BINARY_DIR}/bin)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY
	${PROJECT_BINARY_DIR}/lib)

list(APPEND CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake/Modules/")

set(CMAKE_CXX_STANDARD 17)

###################################################################
# main projects
###################################################################

set(ARGUMENTS_INSTALL_FOLDER ${PROJECT_BINARY_DIR} CACHE INTERNAL "")

add_subdirectory(thirdparty)
add_subdirectory(sim)