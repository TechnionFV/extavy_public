project(extavy)
cmake_minimum_required (VERSION 3.5.1)

if (CMAKE_SOURCE_DIR STREQUAL CMAKE_BINARY_DIR ) 
  message (FATAL_ERROR
    "In-source builds are not allowed. Please clean your source tree and try again.")  
endif()

# This is a really useful scripts that creates options that depends on
# other options. It can even be used with generator expressions !
include(CMakeDependentOption)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_CURRENT_LIST_DIR}/cmake")
include(Coverage)

set(ABC_USE_NAMESPACE "abc" CACHE STRING "Abc namespace to use.")
set(READLINE_FOUND FALSE)

add_subdirectory(abc)
add_subdirectory(minisat)
add_subdirectory(glucose)
add_subdirectory(cadical)
add_subdirectory(muser2)
add_subdirectory(btor2tools)
add_subdirectory(avy)
