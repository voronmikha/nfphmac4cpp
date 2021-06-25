cmake_minimum_required(VERSION 3.19)
project(nfphmac4cpp LANGUAGES CXX)

# ---------------------------------------------------------------------------------------
# Compiler config
# ---------------------------------------------------------------------------------------
if (NOT CMAKE_CXX_STANDARD)
    set(CMAKE_CXX_STANDARD 20)
    set(CMAKE_CXX_STANDARD_REQUIRED ON)
    set(CMAKE_CXX_EXTENSIONS OFF)
endif ()


enable_testing()
add_subdirectory(src)
add_subdirectory(third-party/Catch2)
add_subdirectory(tests)
