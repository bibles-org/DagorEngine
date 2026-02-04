add_library(rapidjson INTERFACE)
add_library(dagor::rapidjson ALIAS rapidjson)

target_include_directories(rapidjson
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)
