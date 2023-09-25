cmake_minimum_required(VERSION 3.22)
project(CMakeTemplateLib)

set(CMAKE_CXX_STANDARD 20)

add_library( CMakeTemplateLib STATIC )

target_sources( CMakeTemplateLib
    PRIVATE
        src/TemplatePrivateClass.h
        src/TemplatePrivateClass.cpp
        src/TemplateSourceFile.cpp
        include/TemplatePublicHeader.h

)

target_include_directories( CMakeTemplateLib
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
    PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src
)
