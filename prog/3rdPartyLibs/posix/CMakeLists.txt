add_library(posix INTERFACE)
add_library(dagor::posix ALIAS posix)

target_include_directories(posix
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)
