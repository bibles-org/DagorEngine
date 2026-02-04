cmake_minimum_required(VERSION 3.20)

project(DagorEngine
        LANGUAGES C CXX
        VERSION 4.2.0
)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


add_compile_options(
        -Wno-unknown-pragmas
        -Wno-deprecated-pragma
        -Wno-unused-parameter

        -fno-exceptions
        -fno-rtti
)

add_compile_definitions(
        _TARGET_PC_LINUX=1
        _TARGET_64BIT=1
)

add_subdirectory(prog)