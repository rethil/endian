enable_testing()

add_subdirectory(catch2)

add_library(runner STATIC
	runner.cpp
)
target_link_libraries(runner
	PUBLIC Catch2
)
target_compile_definitions(runner
	PRIVATE CATCH_CONFIG_MAIN
)


add_executable(xendian_test
	xendian_test.cpp
)
target_link_libraries(xendian_test
	PUBLIC runner
)
