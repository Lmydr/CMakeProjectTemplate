cmake_minimum_required(VERSION 3.22)
project(CMakeProjectTemplate)

set(CMAKE_CXX_STANDARD 20)

add_executable( CMakeProjectTemplate
    main.cpp
)

add_subdirectory( lib )

add_dependencies( CMakeProjectTemplate
    CMakeTemplateLib
)

target_link_libraries( CMakeProjectTemplate
    CMakeTemplateLib
)

link_directories( "${CMAKE_CURRENT_SOURCE_DIR}/_build/lib/CMakeTemplateLib" )
