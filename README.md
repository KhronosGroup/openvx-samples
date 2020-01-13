[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

<p align="center"><img width="50%" src="https://upload.wikimedia.org/wikipedia/en/thumb/d/dd/OpenVX_logo.svg/1920px-OpenVX_logo.svg.png" /></p>

# OpenVX Samples

<a href="https://www.khronos.org/openvx/" target="_blank">Khronos OpenVX™</a> is an open, royalty-free standard for cross-platform acceleration of computer vision applications. OpenVX enables performance and power-optimized computer vision processing, especially important in embedded and real-time use cases such as face, body, and gesture tracking, smart video surveillance, advanced driver assistance systems (ADAS), object and scene reconstruction, augmented reality, visual inspection, robotics and more.

In this project, we provide OpenVX sample applications to use with any conformant implementation of OpenVX.

## Canny Edge Detector Sample

In this sample we will create an OpenVX graph to run canny edge detection on an image or a live camera. This sample application uses <a href="https://en.wikipedia.org/wiki/OpenCV" target="_blank">OpenCV</a> to decode input image and display the output. 

 <p align="center"><img width="60%" src="images/canny_image.PNG" /></p>

### Prerequisites

* [Conformant OpenVX Implementation](https://github.com/KhronosGroup/Khronosdotorg/blob/master/api/openvx/resources.md)

* [OpenCV](https://github.com/opencv/opencv/releases/tag/3.4.0)

### Steps to run the canny sample

* **Step - 1:** Build and install [Conformant OpenVX Implementation](https://github.com/KhronosGroup/OpenVX-sample-impl). In this example we will use the OpenVX Sample Implementation available on [GitHub](https://github.com/KhronosGroup/OpenVX-sample-impl)

```
Build OpenVX on Linux

* Git Clone project with a recursive flag to get submodules

      git clone --recursive https://github.com/KhronosGroup/OpenVX-sample-impl.git

* Use Build.py script

      cd OpenVX-sample-impl/
      python Build.py --os=Linux --arch=64 --conf=Debug --conf_vision --enh_vision --conf_nn
```

* **Step - 2:** Export OpenVX Directory Path

```
export OPENVX_DIR=PATH_TO_OPENVX/OpenVX-sample-impl/install/Linux/x64/Debug
```

* **Step - 3:** Clone the OpenVX Samples project and build the canny application

```
cd ~/ && mkdir OpenVXSample-canny
cd OpenVXSample-canny/
git clone https://github.com/kiritigowda/openvx-samples.git
```

* **Step - 4:** CMake and Build the canny application

```
mkdir canny-build && cd canny-build
cmake -DOPENVX_INCLUDES=$OPENVX_DIR/include -DOPENVX_LIBRARIES=$OPENVX_DIR/bin/libopenvx.so ../openvx-samples/canny-edge-detector/
make
```

* **Step - 5:** Run Canny application

    * **Live**
    
    ```
    ./cannyEdgeDetector --live
    ```


    * **Image**
    
    ````
    ./cannyEdgeDetector --image ../openvx-samples/images/face.png
    ````
 <p align="center"><img src="images/canny-app.png" /></p>
