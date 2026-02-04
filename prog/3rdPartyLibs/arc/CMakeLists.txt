# Compression and archive libraries

# ============================================================================
# FastLZ
# ============================================================================
add_library(fastlz STATIC
        fastlz/fastlz.c
)

add_library(dagor::fastlz ALIAS fastlz)

target_include_directories(fastlz PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/fastlz
)

# ============================================================================
# LZ4
# ============================================================================
add_library(lz4 STATIC
        lz4/lz4.c
        lz4/lz4hc.c
        lz4/lz4frame.c
)

add_library(dagor::lz4 ALIAS lz4)

target_include_directories(lz4 PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/lz4
)

# ============================================================================
# LZMA 9.20
# ============================================================================
add_library(lzma STATIC
        lzma-9.20/LzFind.c
        lzma-9.20/LzmaDec.c
        lzma-9.20/LzmaEnc.c
)

add_library(dagor::lzma ALIAS lzma)

target_include_directories(lzma PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/lzma-9.20
)

# ============================================================================
# zlib-ng (modern zlib)
# ============================================================================
file(GLOB ZLIB_NG_SOURCES
        zlib-ng/*.c
        zlib-ng/arch/x86/*.c  # x86 optimizations
)

add_library(zlib-ng STATIC
        ${ZLIB_NG_SOURCES}
)

add_library(dagor::zlib-ng ALIAS zlib-ng)

target_include_directories(zlib-ng PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/zlib-ng
)

# ============================================================================
# zstd 1.5.7 (use newer version)
# ============================================================================
file(GLOB ZSTD_SOURCES
        zstd-1.5.7/common/*.c
        zstd-1.5.7/compress/*.c
        zstd-1.5.7/decompress/*.c
)

add_library(zstd STATIC
        ${ZSTD_SOURCES}
)

add_library(dagor::zstd ALIAS zstd)

target_include_directories(zstd PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/zstd-1.5.7
)

# ============================================================================
# Brotli
# ============================================================================
file(GLOB BROTLI_SOURCES
        brotli/common/*.c
        brotli/dec/*.c
        brotli/enc/*.c
)

add_library(brotli STATIC
        ${BROTLI_SOURCES}
)

add_library(dagor::brotli ALIAS brotli)

target_include_directories(brotli PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/brotli/include
)