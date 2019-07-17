cmake_minimum_required(VERSION 2.8.3)
project(laser_node)

set(CMAKE_CXX_STANDARD 11)

include_directories(
	include/laser_node
)

add_executable(laser_node src/lms5xx_node.cpp src/SickLMS5xx.cc src/SickLMS5xxBufferMonitor.cc src/SickLMS5xxMessage.cc)
target_link_libraries(laser_node pthread)
