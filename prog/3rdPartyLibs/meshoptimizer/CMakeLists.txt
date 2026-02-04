add_library(meshoptimizer STATIC
        src/allocator.cpp
        src/clusterizer.cpp
        src/indexcodec.cpp
        src/indexgenerator.cpp
        src/overdrawanalyzer.cpp
        src/overdrawoptimizer.cpp
        src/simplifier.cpp
        src/spatialorder.cpp
        src/stripifier.cpp
        src/vcacheanalyzer.cpp
        src/vcacheoptimizer.cpp
        src/vertexcodec.cpp
        src/vertexfilter.cpp
        src/vfetchanalyzer.cpp
        src/vfetchoptimizer.cpp
)

add_library(dagor::meshoptimizer ALIAS meshoptimizer)

target_include_directories(meshoptimizer
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

target_compile_definitions(meshoptimizer
        PRIVATE
        _RELEASE
)
