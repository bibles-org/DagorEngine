add_library(acl INTERFACE)
add_library(dagor::acl ALIAS acl)

target_include_directories(acl
        INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}/includes
)
