add_library(glm INTERFACE)
add_library(dagor::glm ALIAS glm)

target_include_directories(glm
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}
)

