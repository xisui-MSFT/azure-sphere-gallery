#  Copyright (c) Microsoft Corporation. All rights reserved.
#  Licensed under the MIT License.

cmake_minimum_required(VERSION 3.10)

project(OSNetworkRequirementChecker-HLApp C)

azsphere_configure_tools(TOOLS_REVISION "23.05")
azsphere_configure_api(TARGET_API_SET "16")

add_executable(${PROJECT_NAME} main.c eventloop_timer_utilities.c dns-helper.c ntp-helper.c)
target_link_libraries(${PROJECT_NAME} applibs gcc_s c)

azsphere_target_add_image_package(${PROJECT_NAME})
