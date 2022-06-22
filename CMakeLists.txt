cmake_minimum_required(VERSION 3.5)
get_filename_component(PROJECT_NAME ${CMAKE_SOURCE_DIR} NAME)
project(${PROJECT_NAME})

if(MSVC)
	add_compile_options(/W4)
else()	
	add_compile_options(-Wall -Wextra -Wpedantic)
endif()	

add_executable(intro main.cpp)
target_compile_features(intro PRIVATE cxx_lambda_init_captures)


