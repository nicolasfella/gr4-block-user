# list your headers (absolute or relative)
set(MY_HEADERS
        include/gnuradio-4.x/math/math_block0.hpp
        # add more as necessary
)

# if there are C++ sources in e.g. blocks/math/src
file(GLOB MY_MATH_SRCS "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")

add_library(myBlock SHARED ${MY_MATH_SRCS})

gr_generate_block_instantiations(myBlock HEADERS ${MY_HEADERS} SPLIT_BLOCK_INSTANTIATIONS)

set_target_properties(myBlock PROPERTIES CXX_STANDARD 23)
