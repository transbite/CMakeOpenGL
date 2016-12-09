cmake_minimum_required(VERSION 3.5)

project(CMakeOpenGL)
find_package(OpenGL REQUIRED)

if(OPENGL_FOUND)
	message("OpenGL found " ${OPENGL_FOUND})
	message("OpenGL include dir" ${OPENGL_INCLUDE_DIR})

endif()

find_path(GL_INCLUDE_DIR GL/gl.h)
message("GL INCLUDE DIR " ${GL_INCLUDE_DIR})
find_path(GLEW_INCLUDE_DIR GL/glew.h)
find_library(GLEW_LIBRARY NAMES GLEW glew32 glew glew32s)
message("GLEW INCLUDE DIR " ${GLEW_INCLUDE_DIR})
message("GLEW LIBRARY" ${GLEW_LIBRARY})
