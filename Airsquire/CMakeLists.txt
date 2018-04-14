cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(cylinder_segmentation)

set(Boost_DEBUG ON)
set(Boost_USE_STATIC_LIBS ON)
set(Boost_USE_STATIC ON)
set(BOOST_LIBRARYDIR "C:/Users/Jolton/Downloads/boost_1_66_0/boost_1_66_0/stage/lib")
set(BOOST_INCLUDEDIR "C:/Program Files/PCL 1.8.1/3rdParty/Boost/include")

set(OPENNI_LIBRARY_DIRS "C:/Program Files/OpenNI2/Lib")
set(OPENNI_INCLUDE_DIRS "C:/Program Files/OpenNI2/Include")

FIND_PACKAGE(Boost)


find_package(PCL 1.8.1 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (cylinder_segmentation cylinder_segmentation.cpp)
target_link_libraries (cylinder_segmentation ${PCL_LIBRARIES})