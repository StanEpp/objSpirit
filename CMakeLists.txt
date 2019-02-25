cmake_minimum_required(VERSION 3.5)

project(objSpirit VERSION 0.5)
include(GNUInstallDirs)
add_library(objSpirit SHARED
    src/objSpirit.cpp
)

set_target_properties(objSpirit PROPERTIES
    VERSION
        ${PROJECT_VERSION}
    PUBLIC_HEADER
        src/objSpirit.hpp
)

target_link_libraries(objSpirit boost_filesystem boost_system)

install(TARGETS objSpirit
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

