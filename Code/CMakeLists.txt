include_directories(${CMAKE_CURRENT_SOURCE_DIR})

set(CMAKE_CXX_STANDARD 11)

add_definitions(-D__LINUX__)

set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -DDEBUG")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_DEBUG} -DRELEASE")

if(UNIX)
    add_compile_options(-Wall -Werror -Wfatal-errors)
    add_compile_options(-Wno-invalid-offsetof)
endif()

add_definitions(-DDEBUG)

add_subdirectory(Core)
add_subdirectory(TestFramework)
add_subdirectory(Tools)
