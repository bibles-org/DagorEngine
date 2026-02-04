add_library(utf8 INTERFACE)

add_library(dagor::utf8 ALIAS utf8)

target_include_directories(utf8
        INTERFACE
        utf8
)
