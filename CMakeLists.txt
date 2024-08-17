cmake_minimum_required(VERSION 3.21)
project(RapidJSON VERSION "1.1.0" LANGUAGES CXX)

# add_definitions(-DRAPIDJSON_USE_MEMBERSMAP=1)

add_library(rapidjsonlib INTERFACE)

target_include_directories(rapidjsonlib INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")

target_compile_definitions(rapidjsonlib PRIVATE RAPIDJSON_HAS_STDSTRING)

set_target_properties(rapidjsonlib PROPERTIES
	CMAKE_CXX_EXTENSIONS OFF
	LINKER_LANGUAGE CXX)
