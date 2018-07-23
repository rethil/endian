project(xendian)
cmake_minimum_required(VERSION 3.5)

option(XENDIAN_BUILD_TESTS "Enable tests" OFF)

add_subdirectory(src)

if (${XENDIAN_BUILD_TESTS})
	add_subdirectory(test)
endif()
