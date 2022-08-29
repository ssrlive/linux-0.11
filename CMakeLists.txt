project(linux)

file(GLOB LINUX_SRC
    "init/main.c"
    "fs/*.c"
    "kernel/*/*.c"
    "lib/*.c"
    "mm/*.c"
    "tools/build.c"
    )

include_directories(
    "include",
    "include/asm",
    "include/linux",
    "include/sys",
)

add_executable(linux ${LINUX_SRC})
