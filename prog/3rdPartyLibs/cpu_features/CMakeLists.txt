add_library(cpu_features STATIC
        src/filesystem.c
        src/stack_line_reader.c
        src/string_view.c
        src/impl_aarch64_cpuid.c

        src/impl_x86_linux_or_android.c
        src/impl_loongarch_linux.c
        src/impl_ppc_linux.c
        src/impl_riscv_linux.c
        src/impl_s390x_linux.c
        src/impl_aarch64_freebsd.c
)

add_library(dagor::cpu_features ALIAS cpu_features)

target_include_directories(cpu_features
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
        ${CMAKE_CURRENT_SOURCE_DIR}/include/internal
)

target_compile_definitions(cpu_features
        PRIVATE
        STACK_LINE_READER_BUFFER_SIZE=1024
)
