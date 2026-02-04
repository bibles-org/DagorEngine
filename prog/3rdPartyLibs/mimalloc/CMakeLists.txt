add_library(mimalloc STATIC
        src/alloc.c
        src/alloc-aligned.c
        src/alloc-posix.c
        src/arena.c
        src/bitmap.c
        src/heap.c
        src/init.c
        src/libc.c
        src/options.c
        src/os.c
        src/page.c
        src/random.c
        src/segment.c
        src/segment-map.c
        src/stats.c
        src/prim/unix/prim.c
)

add_library(dagor::mimalloc ALIAS mimalloc)

target_include_directories(mimalloc
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_definitions(mimalloc
        PRIVATE
        MI_DEBUG=0
)
