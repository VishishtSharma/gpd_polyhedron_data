Author: Vishisht Sharma
SN: 220768065
-----------------------------INFORMATION------------------------------------

-The gpd folder contains the source code for GPD Framework.(Needs to be cloned from Github)
- misc.ipynb is the python script that scales the input models to work with GPD and introduces Gaussian Noise.
- To install CloudCompare, use flatpak
	- flatpak install flathub org.cloudcompare.CloudCompare"


-------------------------------INSTALLATION---------------------------------
- Requirements
-PCL 1.9 or newer
-Eigen 3.0 or newer
-OpenCV 3.4 or newer
-ROS Kinetic (Optional)



The following instructions have been tested on Ubuntu 16.04 with ROS Kinetic. Similar instructions should work for other Linux distributions.


-------Open a terminal in the "code" folder ---------

- git clone https://github.com/atenpas/gpd
- cd gpd
- mkdir build && cd build
- cmake -DCMAKE_BUILD_TYPE=DEBUG -DCMAKE_CXX_FLAGS_DEBUG="-O3 -march=native -mtune=intel -msse4.2 -mavx2 -mfma -flto -fopenmp -fPIC -Wno-deprecated -Wenum-compare -Wno-ignored-attributes -std=c++17" .. 
- make -j4

This compiles the GPD and then we can use the "misc.ipynb" with CloudCompare to generate point clouds (.pcd files)
--------------------------------------------------------------------------


