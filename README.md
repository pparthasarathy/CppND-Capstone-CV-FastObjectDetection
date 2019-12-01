# CppND-Capstone-CV-FastObjectDetection
Computer Vision: Deep Learning based Fast Object Detection using YOLOv3 with OpenCV backend

<img src="data/hotdogFork_out.jpg" width = 400 height = 300/>

## Dependencies for Running Locally
* cmake >= 2.8
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* OpenCV >= 4.1 with pkg-config and extra opencv_contrib modules
  * Build/ Install OpenCV from Official Source: Use install script `opencv-install.sh` to build and install from the official OpenCV source code can be found [here](https://github.com/opencv/opencv). Use commands: `sudo chmod a+x opencv-install.sh` and `./opencv-install.sh`. This has only been tried on Ubuntu 18.04 from `/home/usr/` path. We will assume this path in further instructions
  * Find path of OpenCV Libraries with `sudo updatedb` and `locate libopencv_highgui.so.3.4`, which in my case was `/home/usr/installation/OpenCV-3.4/lib`
  * Add OpenCV Library path to newly created file `/etc/ld.so.conf.d/opencv.conf`. File should have a single line with `/home/usr/installation/OpenCV-3.4/lib`
  * Ensure this gets included with `sudo ldconfig -v`
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* Get YOLOv3 Object Detection Model
  * Use getYOLOv3.sh script with commands: `sudo chmod a+x getYOLOv3.sh` and `./getYOLOv3.sh`
  * This gets the model with pre-trained weights, configuration data, and class names

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory in the top level directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`

## Test Instructions
1. Run it on image: `./obj_detect.out --image=hotdogFork.jpg`. Apart from displaying the result, a new output file `hotdogFork_out.jpg` is created with objects detected by a bounding box and a probability match with the class detected
2. Run it on video: `./obj_detect.out --video=marathon.mp4`. Apart from displaying results, a new ouput file `marathon_out.avi` is created with objects detected by a bounding box and a probability match with the class detected
