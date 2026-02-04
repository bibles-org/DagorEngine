add_library(jsonsl STATIC
        jsonsl.c
)

add_library(dagor::jsonsl ALIAS jsonsl)

target_include_directories(jsonsl
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}
)
