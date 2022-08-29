project(linux)

file(GLOB LINUX_SRC
    "boot/*.s"
    "init/main.c"
    "fs/*.c"
    "kernel/*.c"
    "kernel/*.s"
    "kernel/blk_drv/*.c"
    "kernel/chr_drv/*.c"
    "kernel/chr_drv/*.s"
    "kernel/math/*.c"
    "lib/*.c"
    "mm/*.c"
    "mm/*.s"
    "tools/build.c"
    )

include_directories(
    "include",
    "include/asm",
    "include/linux",
    "include/sys",
)

add_executable(linux ${LINUX_SRC})
