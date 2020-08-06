cmake_minimum_required (VERSION 3.12)

project (dgg-svg VERSION 1.0)

add_executable(DGG_Precompute

  src/dgg_buffer.h
	src/dgg_time.h
	src/dgg_definition.h
	src/DGG_Precompute/dgg_precompute.h
	src/DGG_Precompute/FastDGG.h
	src/DGG_Precompute/SVG.h
	src/ICH/BaseModel.h
	src/ICH/ExactMethodForDGP.h
	src/ICH/ImprovedCHWithEdgeValve.h
	src/ICH/Point3D.h
	src/ICH/PreviousCH.h
	src/ICH/RichModel.h

  src/DGG_Precompute/main.cpp
	src/DGG_Precompute/FastDGG.cpp
	src/DGG_Precompute/SVG.cpp
	src/DGG_Precompute/dgg_precompute.cpp
	src/ICH/BaseModel.cpp
	src/ICH/ExactMethodForDGP.cpp
	src/ICH/ImprovedCHWithEdgeValve.cpp
	src/ICH/Point3D.cpp
	src/ICH/PreviousCH.cpp
	src/ICH/RichModel.cpp
)

set_target_properties(DGG_Precompute PROPERTIES CXX_STANDARD 17 CXX_STANDARD_REQUIRED YES)
target_include_directories(DGG_Precompute PRIVATE src)

add_executable(DGG_Solution

	src/dgg_buffer.h
	src/dgg_definition.h
	src/dgg_dijkstra.h
	src/dgg_time.h
	src/ICH/BaseModel.h
	src/ICH/Point3D.h
	src/ICH/RichModel.h

  src/DGG_Solution/dgg_solution.cpp
	src/ICH/BaseModel.cpp
	src/ICH/Point3D.cpp
	src/ICH/RichModel.cpp
)

set_target_properties(DGG_Solution PROPERTIES CXX_STANDARD 17 CXX_STANDARD_REQUIRED YES)
target_include_directories(DGG_Solution PRIVATE src)
