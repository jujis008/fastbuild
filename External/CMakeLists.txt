add_library(lz4 STATIC
    LZ4/lz4-r127/lz4.c
    LZ4/lz4-r127/xxhash.c)
target_include_directories(lz4 PUBLIC LZ4/lz4-r127)
