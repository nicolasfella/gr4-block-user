cmake_minimum_required(VERSION 3.30)

# find_package(BlockLib REQUIRED)

include(FetchContent)

FetchContent_Declare(
  block
  GIT_REPOSITORY https://github.com/nicolasfella/gr4-blocklib-build-concept.git
  GIT_TAG        stuff
)

FetchContent_MakeAvailable(block)

add_subdirectory(myblock)
