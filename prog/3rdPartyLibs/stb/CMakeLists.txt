add_library(stb INTERFACE)
add_library(dagor::stb ALIAS stb)

target_include_directories(stb
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}
)
