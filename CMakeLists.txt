cmake_minimum_required(VERSION 3.5)

project(CMakeOpenGL)
find_package(OpenGL REQUIRED)

set(Name_VAR_1 "TestVar1" CACHE STRING "Asdf")
set(Name_VAR_2 False CACHE BOOL "bnm cs ")
set(Name_VAR_3 "C:/" CACHE FILEPATH "cms ww d")

option(Name_VAR_4 Bool False)
option(Name_VAR_5 Bool True)
#option(TEST_VAR_6 String "TestVar6")
#option(TEST_VAR_7 Path "C:/")

if(OPENGL_FOUND)
	message("OpenGL found " ${OPENGL_FOUND})
	message("OpenGL include dir" ${OPENGL_INCLUDE_DIR})

endif()

find_path(GL_INCLUDE_DIR GL/gl.h)
message("GL INCLUDE DIR " ${GL_INCLUDE_DIR})
find_path(GLEW_INCLUDE_DIR GL/glew.h)
find_library(GLEW_LIBRARY NAMES GLEW glew32 glew glew32s)
find_library(GL_C_LIBRARY NAMES GL opengl32)
message("GLEW INCLUDE DIR " ${GLEW_INCLUDE_DIR})
message("GLEW LIBRARY " ${GLEW_LIBRARY})
message("GL_C_LIBRARY " ${GL_C_LIBRARY})

