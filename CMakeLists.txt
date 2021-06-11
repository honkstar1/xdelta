cmake_minimum_required(VERSION 3.1)
project(xdelta C)

#-------------------------------------------------------------------------------------------
# Library definition
#-------------------------------------------------------------------------------------------
file(GLOB XDELTA_SOURCES "xdelta3/xdelta3.c")
file(GLOB XDELTA_HEADERS "xdelta3/*.h")
add_library(xdelta ${XDELTA_SOURCES} ${XDELTA_HEADERS})

#-------------------------------------------------------------------------------------------
# Include dirs
#-------------------------------------------------------------------------------------------
target_include_directories(xdelta PUBLIC xdelta3)

#target_link_libraries(xdelta lzma)

#add_compile_definitions(SIZEOF_SIZE_T=8 SIZEOF_UNSIGNED_LONG_LONG=8 _WIN32=1 XD3_USE_LARGEFILE64=1 SECONDARY_DJW=1 SECONDARY_LZMA=1 SECONDARY_FGK=1 XD3_WIN32=1 LZMA_API_STATIC)
add_compile_definitions(SIZEOF_SIZE_T=8 SIZEOF_UNSIGNED_LONG_LONG=8 _WIN32=1 XD3_USE_LARGEFILE64=1 SECONDARY_DJW=1 SECONDARY_FGK=1 XD3_WIN32=1)
