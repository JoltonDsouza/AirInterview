# Airsquire-AirInterview

## Interview PCL Problem Statement

By using table_scene_mug_stereo_textured.pcd, find the cylinder object inside the scene

## Solution

1) The solution file is generated using CMAKE. 
2) The CMAKE.list file included in the repository is used to generate the build files. 

## NOTE ##
Platform versions have to be taken into consideration while performing the task on Windows System, as PCL has a lot of dependencies.

## Steps

1) Download the Qt(ver 4.8.0), Cmake, PCL latest version(PCL 1.8.1 All-in-one Installer MSVC2017 x64) zip files and install them on the system. PCL installation includes OpenNI2(OpenNI for lower versions of msvc) setup.
2) Build files using CMAKE.
3) Debug on Microsoft Visual Studio 2017.
4) Visualize the .pcd files by making essential changes in the cylinder_segmentation.cpp file.


## Challenges

1) Long path error: Installing PCL can create 'PATH too long installer unable to modify path' an error. This can be solved by manually providing the path to the environment variables.
2) 'Boost not found' error: This error occurs if the Boost 'stage/lib' is missing in the newer versions of Boost(ver 1.66.0). Following the tutorial helps. 'Bootstrapping' boost on cmd is a necessary step and executing the 'bjam' application file hence created, is crucial to eliminate the error. This creates the 'stage' directory and its path has to be provided in the CMAKE.list file for the Boost Lib directory.
3) Eigen file error: This error occurs in the 'eigen.h' file as 'Eigen::internal' used in the script throws an error. Replacing 'Eigen::internal' with either 'std' or 'pcl' solves it. Eg. 'Eigen::internal::sqrt' with 'std::sqrt'.
4) Rest errors were tackled by debugging with prior C++ knowledge.
5) Visualization: To visualize the data, a lot of documentation had to be read on the pcl website and forums, link -> http://www.pcl-users.org/Visualizer-to-a-PCD-file-td4036171.html
