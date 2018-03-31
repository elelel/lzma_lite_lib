cmake_minimum_required(VERSION 3.2 FATAL_ERROR)

project(lzma LANGUAGES C)

set(SOURCES
  ${CMAKE_CURRENT_SOURCE_DIR}/lzma/LzmaDec.c
  ${CMAKE_CURRENT_SOURCE_DIR}/lzma/LzmaEnc.c
  ${CMAKE_CURRENT_SOURCE_DIR}/lzma/LzFind.c)

add_library(lzma STATIC ${SOURCES})
target_compile_definitions(lzma PRIVATE "_7ZIP_ST")
