add_library(jsoncpp STATIC)

target_sources(jsoncpp PRIVATE
        src/json_value.cpp
        src/json_reader.cpp
        src/json_writer.cpp
)

target_include_directories(jsoncpp PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_features(jsoncpp PUBLIC cxx_std_11)

target_compile_definitions(jsoncpp PUBLIC
        STD_JSONCPP_INCLUDED=1
)