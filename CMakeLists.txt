cmake_minimum_required(VERSION 3.0)

project(libmime VERSION 1.0.0 LANGUAGES C)

add_library(mime SHARED
    src/mime.c
)

set_target_properties(mime PROPERTIES
    VERSION ${PROJECT_VERSION}
    SOVERSION 1
    PUBLIC_HEADER src/mime.h
)

include(GNUInstallDirs)
install(TARGETS mime
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)

