cmake_minimum_required(VERSION 3.21)
project(RapidJSON VERSION "1.1.0" LANGUAGES CXX)

add_library(rapidjsonlib INTERFACE)

target_compile_definitions(rapidjsonlib INTERFACE RAPIDJSON_HAS_STDSTRING=1) # RAPIDJSON_USE_MEMBERSMAP=1

target_include_directories(rapidjsonlib INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")

set_target_properties(rapidjsonlib PROPERTIES
	CMAKE_CXX_EXTENSIONS OFF
	LINKER_LANGUAGE CXX)
