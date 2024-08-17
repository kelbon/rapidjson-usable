cmake_minimum_required(VERSION 3.21)

add_definitions(-DRAPIDJSON_HAS_STDSTRING)

# add_definitions(-DRAPIDJSON_USE_MEMBERSMAP=1)

add_library(rapidjsonlib INTERFACE)

target_include_directories(rapidjsonlib INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")

set_target_properties(rapidjsonlib PROPERTIES
	CMAKE_CXX_EXTENSIONS OFF
	LINKER_LANGUAGE CXX)
