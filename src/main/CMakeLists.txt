
add_executable(ps2_primer
	# Elfldr core
	main.cpp
)


# -Wl,--start-group -lc_nano -lkernel -lps2sdkc -Wl,--end-group

# This ugliness is so we don't link anything we don't need.
# We also prefer/use nano Newlib, to make the executable even smaller.
target_link_libraries(ps2_primer
	"-nodefaultlibs"
	"-Wl,--start-group"
	
	# System libraries
	c_nano
	kernel
	ps2sdkc

	# Project libraries
	"-Wl,--end-group")

# Make the binary output in the root of the build directory, mostly for ease.
set_target_properties(ps2_primer PROPERTIES
	RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}
	CXX_STANDARD 20
	CXX_EXTENSIONS ON
	CXX_STANDARD_REQUIRED ON
)
