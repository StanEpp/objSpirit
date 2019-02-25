cmake_minimum_required(VERSION 3.5)

project(objSpirit VERSION 0.5)

find_package(Boost REQUIRED)

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

configure_file(objSpirit.pc.in objSpirit.pc @ONLY)

target_include_directories(objSpirit PRIVATE .)
target_link_libraries(objSpirit boost_filesystem boost_system)

install(TARGETS objSpirit
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR})

install(FILES ${CMAKE_BINARY_DIR}/objSpirit.pc
    DESTINATION ${CMAKE_INSTALL_DATAROOTDIR}/pkgconfig)
