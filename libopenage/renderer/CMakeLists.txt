add_sources(libopenage
	color.cpp
	geometry.cpp
	renderer.cpp
	sdl_global.cpp
	shader_program.cpp
	tests.cpp
	text.cpp
	texture.cpp
	texture_array.cpp
	uniform_input.cpp
	util.cpp
	window.cpp
)

pxdgen(
	tests.h
)

add_subdirectory(font/)
add_subdirectory(resources/)

if(OPENGL_FOUND)
    add_subdirectory(opengl/)
endif()

if(VULKAN_FOUND)
    add_subdirectory(vulkan/)
endif()
