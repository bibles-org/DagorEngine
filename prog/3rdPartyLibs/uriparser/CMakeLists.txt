add_library(uriparser STATIC
        src/UriCommon.c
        src/UriCompare.c
        src/UriEscape.c
        src/UriFile.c
        src/UriIp4Base.c
        src/UriIp4.c
        src/UriMemory.c
        src/UriNormalizeBase.c
        src/UriNormalize.c
        src/UriParseBase.c
        src/UriParse.c
        src/UriQuery.c
        src/UriRecompose.c
        src/UriResolve.c
        src/UriShorten.c
)

target_include_directories(uriparser
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
        ${CMAKE_CURRENT_SOURCE_DIR}/src
)

target_compile_definitions(uriparser
        PRIVATE
        URI_STATIC_BUILD
        URI_NO_UNICODE
)

set_target_properties(uriparser PROPERTIES
        POSITION_INDEPENDENT_CODE ON
)
