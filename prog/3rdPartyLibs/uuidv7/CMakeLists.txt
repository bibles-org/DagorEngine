add_library(uuidv7 STATIC
        uuidv7.cpp
)

add_library(dagor::uuidv7 ALIAS uuidv7)

target_include_directories(uuidv7
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}
)