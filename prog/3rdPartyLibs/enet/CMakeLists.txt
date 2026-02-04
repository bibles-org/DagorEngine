add_library(enet STATIC
        callbacks.c
        compress.c
        host.c
        list.c
        packet.c
        peer.c
        protocol.c
        unix.c
)

add_library(dagor::enet ALIAS enet)

target_include_directories(enet
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_definitions(enet
        PRIVATE
        HAS_SOCKLEN_T
        HAS_POLL
        HAS_INET_NTOP
        HAS_INET_PTON
        HAS_MSGHDR_FLAGS
        SOMAXCONN=128
)

target_compile_options(enet
        PRIVATE
        -Wno-unused-parameter
)
