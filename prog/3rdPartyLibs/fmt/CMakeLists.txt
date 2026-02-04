add_library(fmt STATIC
        src/format.cc
)

add_library(dagor::fmt ALIAS fmt)

target_include_directories(fmt
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_definitions(fmt
        PRIVATE
        FMT_UNICODE=0
)

target_compile_options(fmt
        PRIVATE
        -fexceptions
)
