# OpenCV-compile
Compiling OpenCV 3.X with CUDA and FFMpeg on Ubuntu 16.04


Goal: Compile OpenCV 3.X using CUDA and FFMpeg to accelerate Deep Learning applications consisting image/video processing

 

Environment:

Operating System => Linux Ubuntu 16.04 LTS
Python => Anaconda Python 3.5.4
CUDA =>  release 9.0, V9.0.176
OpenCV => 3.3.1

 

GPU and OpenCV

GPU-accelerated computing offloads compute-intensive portions of the application to the GPU, while the remainder of the code still runs on the CPU. From a user's perspective, applications simply run much faster.
Significant part of Computer Vision is image processing, the area that graphics accelerators were originally designed for. Other parts also support massive parallel computations and often naturally map to GPU architectures. 
OpenCV GPU module is written using CUDA, therefore it benefits from the CUDA ecosystem.
The GPU module is designed as host API extension. This design provides the user an explicit control on how data is moved between CPU and GPU memory. Although the user has to write some additional code to start using the GPU, this approach is both flexible and allows more efficient computations. In general, it is a good idea to develop the application using the CPU part of OpenCV, and then accelerate it with the GPU module.

FFMpeg and OpenCV

OpenCV can use the FFmpeg library (http://ffmpeg.org/) as backend to record, convert and stream audio and video. FFMpeg is a complete, cross-reference solution. If you enable FFmpeg while configuring OpenCV, then CMake will download and install the binaries in OPENCV_SOURCE_CODE/3rdparty/ffmpeg/. To use FFMpeg at runtime, you must deploy the FFMepg binaries with your application.

 
Install OpenCV 3.3 with Cuda 9.0
 
Prerequisites:
 

1. Python environment (anaconda/conda).

2. CUDA 9.0 libraries installed

 

All the details and steps can be found at following location:
https://www.cerebrumedge.com/single-post/2017/12/26/Compiling-OpenCV-with-CUDA-and-FFMpeg-on-Ubuntu-1604
