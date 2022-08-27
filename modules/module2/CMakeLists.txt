add_library(module2 STATIC)
add_dependencies(module2 module1)

target_link_libraries(module2 module1)
target_sources(module2 PRIVATE
	src/test.cpp
)

target_include_directories(module2 PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")

if(MSVC)
  target_compile_options(module2 PRIVATE /W4 /WX)
else()
  target_compile_options(module2 PRIVATE -Wall -Wextra -Wpedantic -Werror)
endif()