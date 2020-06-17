add_library(thirdPartyLib
	    cgltf.c
	    cgltf.h
	    stb_image.c
	    stb_image.h
	    stb_image_resize.c
	    stb_image_resize.h
	    stb_image_write.c
	    stb_image_write.h
	    stl_reader.h
	    tiny_obj_loader.cpp
	    tiny_obj_loader.h)

target_include_directories(thirdPartyLib PUBLIC 
			   "${CMAKE_CURRENT_SOURCE_DIR}")
