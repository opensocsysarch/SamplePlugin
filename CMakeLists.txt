# Sample Plugin Top-Level CMake
#
# Copyright (C) 2017-2020 Tactical Computing Laboratories, LLC
# All Rights Reserved
# contact@tactcomplabs.com
#
# See LICENSE in the top level directory for licensing details
#
cmake_minimum_required(VERSION 3.4.3)
project(SamplePlugin)
set(VERSION "0.2.0")

#------------------------------------------------------------------------
#-- COREGEN OPTIONS
#------------------------------------------------------------------------
execute_process(COMMAND coregen-config -I OUTPUT_VARIABLE COREGEN_INCLUDE_PATH OUTPUT_STRIP_TRAILING_WHITESPACE)
execute_process(COMMAND coregen-config -K OUTPUT_VARIABLE COREGEN_LINK_PATH OUTPUT_STRIP_TRAILING_WHITESPACE)

message(STATUS "SETTING COREGEN_INCLUDE_PATH=${COREGEN_INCLUDE_PATH}")
message(STATUS "SETTING COREGEN_LINK_PATH=${COREGEN_LINK_PATH}")

#------------------------------------------------------------------------
#-- COMPILER OPTIONS
#------------------------------------------------------------------------
# Require C++11
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O3 -std=c++14 -Wall")
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -O0 -Wall")
set(CMAKE_CXX_FLAGS_RELEASE "${CMAKE_CXX_FLAGS_RELEASE} -O3 -Wall")

add_subdirectory(archive)
add_subdirectory(src)

# EOF
