CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
PROJECT(MINOTAUR)


#SET(OSG_INSTALL_DIR /home/OSG/installs/linux64stat)
#SET(OSG_LIB_DIR ${OSG_INSTALL_DIR}/lib64)
#SET(OSG_PLUGINS_LIB_DIR ${OSG_LIB_DIR}/osgPlugins-3.2.1)
#SET(OSG_INCLUDE_DIR ${OSG_INSTALL_DIR}/include)

#SET(MY_OSG_LIBS osgViewer osgText osgGA osgdb_tiff osgdb_png png osgdb_3ds osgUtil osgDB osgUtil osg OpenThreads)

SET(CEGUI_INSTALL_DIR /home/CEGUI/install)
#SET(CEGUI_LIB_DIR ${CEGUI_INSTALL_DIR}/lib)
SET(CEGUI_INCLUDE_DIR ${CEGUI_INSTALL_DIR}/include/cegui-0)

#SET(MY_CEGUI_LIBS CEGUIBase-0_Static CEGUIOpenGLRenderer-0_Static
	#CEGUICoreWindowRendererSet_Static CEGUIExpatParser_Static
	#CEGUIFreeImageImageCodec_Static CEGUILuaScriptModule-0_Static tolua freeimage freetype GL
	#GLEW expat)

SET(CMAKE_CXX_FLAGS "-Wall -pedantic-errors -std=c++11")

SET(MINOTAUR_ROOT_DIR ${CMAKE_CURRENT_SOURCE_DIR})

SET(MINOTAUR_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)
SET(MINOTAUR_SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
SET(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/CMakeModules)


INCLUDE(Minotaur)


#--------INCLUDES--------#
#------------------------#

INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/include)
#INCLUDE_DIRECTORIES(${OSG_INCLUDE_DIR})
INCLUDE_DIRECTORIES(${CEGUI_INCLUDE_DIR})
INCLUDE_DIRECTORIES(/usr/include/lua5.1)

INCLUDE_DIRECTORIES(${INCLUDE_ROOT_DIR})


ADD_SUBDIRECTORY(src)


