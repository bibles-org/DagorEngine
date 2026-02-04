add_library(eastl STATIC
        source/allocator_eastl.cpp
        source/assert.cpp
        source/atomic.cpp
        source/fixed_pool.cpp
        source/hashtable.cpp
        source/intrusive_list.cpp
        source/numeric_limits.cpp
        source/red_black_tree.cpp
        source/string.cpp
        source/thread_support.cpp

        mem.cpp
        snprintf.cpp
)

add_library(dagor::eastl ALIAS eastl)

target_include_directories(eastl
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_definitions(eastl
        PRIVATE
        EA_COMPILER_NO_EXCEPTIONS
        EA_COMPILER_NO_RTTI
)
