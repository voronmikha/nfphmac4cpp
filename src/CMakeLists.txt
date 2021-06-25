cmake_minimum_required(VERSION 3.19)
#TODO: Добавить версию
project(nfphmac LANGUAGES CXX)
set(TARGET_NAME cpp8583lib)
# ---------------------------------------------------------------------------------------
# Compiler config
# ---------------------------------------------------------------------------------------
#if (NOT CMAKE_CXX_STANDARD)
#    set(CMAKE_CXX_STANDARD 20)
#    set(CMAKE_CXX_STANDARD_REQUIRED ON)
#endif ()
#
#set(CMAKE_CXX_EXTENSIONS OFF)
#
#if (CMAKE_SYSTEM_NAME MATCHES "CYGWIN" OR CMAKE_SYSTEM_NAME MATCHES "MSYS")
#    set(CMAKE_CXX_EXTENSIONS ON)
#endif ()

add_library(${TARGET_NAME})

#target_include_directories(${TARGET_NAME}
#        INTERFACE ./)

#install(TARGETS ${TARGET_NAME}
#        ARCHIVE DESTINATION lib/)
