cmake_minimum_required(VERSION 3.1)
project(nxsbuild)

include_directories(../../../vcglib ../../../vcglib/eigenlib)


SET(HEADERS
	../../../vcglib/wrap/system/qgetopt.h
	../../../vcglib/wrap/ply/plylib.h
	../common/signature.h
	../common/cone.h
	../common/virtualarray.h
	meshstream.h
	meshloader.h
	plyloader.h
	partition.h
	kdtree.h
	trianglesoup.h
	mesh.h
	tsploader.h
	nexusbuilder.h
	objloader.h
	tmesh.h
	vertex_cache_optimizer.h
	texpyramid.h
)

SET(SOURCES
	../../../vcglib/wrap/system/qgetopt.cpp
	../../../vcglib/wrap/ply/plylib.cpp
	../common/virtualarray.cpp
	../common/cone.cpp
	main.cpp
	meshstream.cpp
	meshloader.cpp
	plyloader.cpp
	kdtree.cpp
	mesh.cpp
	tsploader.cpp
	nexusbuilder.cpp
	objloader.cpp
	tmesh.cpp
	texpyramid.cpp
)

cmake_minimum_required(VERSION 3.1)

project(nxsbuild)

set(CMAKE_INCLUDE_CURRENT_DIR ON)
set(CMAKE_AUTOMOC ON)

find_package(Qt5Widgets)

add_executable(nxsbuild ${SOURCES} ${HEADERS})

target_link_libraries(nxsbuild Qt5::Widgets)

