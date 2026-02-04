add_library(bencode STATIC
        bencode.c
)

add_library(dagor::bencode ALIAS bencode)

target_include_directories(bencode
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}
)
