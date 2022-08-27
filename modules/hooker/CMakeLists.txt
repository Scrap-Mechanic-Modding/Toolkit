add_library(hooker STATIC)

target_sources(hooker PRIVATE
	src/test.cpp
)

target_include_directories(hooker PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

if(MSVC)
  target_compile_options(hooker PRIVATE /W4 /WX)
else()
  target_compile_options(hooker PRIVATE -Wall -Wextra -Wpedantic -Werror)
endif()