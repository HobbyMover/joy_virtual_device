cmake_minimum_required(VERSION 3.0)
project(joy_server)

###############################################################################
## file globbing ##############################################################
###############################################################################

# these instructions search the directory tree when CMake is
# invoked and put all files that match the pattern in the variables
# `sources` and `data`
file(GLOB_RECURSE sources main.cpp)
message(sources="${sources}")

# you can use set(sources src/main.cpp) etc if you don't want to
# use globbing to find files automatically

###############################################################################
## target definitions #########################################################
###############################################################################

# add the data to the target, so it becomes visible in some IDE
add_executable(bin ${sources})
#target_include_directories(target PUBLIC input_processing joy_client)

# just for example add some compiler flags
#target_compile_options(target PUBLIC -std=c++14 -Wall -Wfloat-conversion)
