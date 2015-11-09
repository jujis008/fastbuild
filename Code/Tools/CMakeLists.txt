FILE(GLOB_RECURSE TOOL_CORE_SOURCES
    RELATIVE ${CMAKE_CURRENT_SOURCE_DIR}
    "FBuild/FBuildCore/*.cpp")

add_executable(FBuild FBuild/FBuildApp/Main.cpp ${TOOL_CORE_SOURCES})
target_link_libraries(FBuild lz4 Core pthread)
