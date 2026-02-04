add_library(nanosvg INTERFACE)
add_library(dagor::nanosvg ALIAS nanosvg)

target_include_directories(nanosvg
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}
)
