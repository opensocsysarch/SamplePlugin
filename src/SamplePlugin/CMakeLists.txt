# src/SamplePlugin CMakeLists.txt
#
# Copyright (C) 2017-2020 Tactical Computing Laboratories, LLC
# All Rights Reserved
# contact@tactcomplabs.com
#
# See LICENSE in the top level directory for licensing details
#

set(PluginSrcs
SamplePlugin.cpp
SamplePlugin.h
)

message(STATUS "USING COREGEN_INCLUDE_PATH=${COREGEN_INCLUDE_PATH}")

include_directories(${COREGEN_INCLUDE_PATH})

link_directories(${COREGEN_LINK_PATH})

add_library(SamplePlugin SHARED ${PluginSrcs})

target_link_libraries(SamplePlugin CoreGenPluginImpl CoreGenBackend)

install(TARGETS SamplePlugin DESTINATION plugins/SamplePlugin)
install(DIRECTORY "."
        DESTINATION "plugins/SamplePlugin"
        FILES_MATCHING
        PATTERN "*.h")
