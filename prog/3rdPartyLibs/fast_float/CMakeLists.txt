add_library(fast_float INTERFACE)

add_library(dagor::fast_float ALIAS fast_float)

target_include_directories(fast_float
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}
)
