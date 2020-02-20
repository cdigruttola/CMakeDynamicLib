cmake_minimum_required (VERSION 3.10)

set(TRY_LIB_SRC TryLib.cpp)

add_library(lib_dynamic SHARED ${TRY_LIB_SRC})
add_library(lib_static STATIC ${TRY_LIB_SRC})

set_target_properties(lib_dynamic PROPERTIES OUTPUT_NAME "tryLib")
set_target_properties(lib_static PROPERTIES OUTPUT_NAME "staticLib")

set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)

install(TARGETS lib_dynamic lib_static 
	LIBRARY DESTINATION /prova/lib 
	ARCHIVE DESTINATION /prova/lib
	RUNTIME DESTINATION /prova/bin)

install(DIRECTORY ../include/ DESTINATION /prova/include)
