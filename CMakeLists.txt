
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS ON)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -lpthread -no-pie -fPIC -std=c++11")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fPIC")

add_subdirectory("thirdparty")

add_library(xatlasLib
	    xatlas/xatlas.cpp
	    xatlas/xatlas.h
	    )

target_include_directories(xatlasLib PUBLIC 
			   "${CMAKE_CURRENT_SOURCE_DIR}/xatlas")

target_link_libraries(xatlasLib PUBLIC
		      thirdPartyLib)
