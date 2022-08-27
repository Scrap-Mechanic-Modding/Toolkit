add_library(module1 STATIC)


target_sources(module1 PRIVATE
	src/test.cpp
)

target_include_directories(module1 PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

if(MSVC)
  target_compile_options(module1 PRIVATE /W4 /WX)
else()
  target_compile_options(module1 PRIVATE -Wall -Wextra -Wpedantic -Werror)
endif()