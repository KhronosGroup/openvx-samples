[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

<p align="center"><img width="50%" src="https://upload.wikimedia.org/wikipedia/en/thumb/d/dd/OpenVX_logo.svg/1920px-OpenVX_logo.svg.png" /></p>

# OpenVX Samples

OpenVX Samples to use with any conformant implementation of OpenVX

## Canny Edge Detector Sample

 <p align="center"><img width="60%" src="images/canny_image.PNG" /></p>

Use the commands below to build and run canny edge detector live or on any image

### Prerequisites
* Conformant OpenVX Implementation
* OpenCV - for reading and displaying images

### Steps to run the canny sample

* Build and install [Conformant OpenVX Implementation](https://github.com/KhronosGroup/OpenVX-sample-impl)

* Export OpenVX Directory Path

```
export OPENVX_DIR=PATH_TO_OPENVX/OpenVX-sample-impl/install/Linux/x64/Debug
```

* Build the Canny Sample

```
cmake -DOPENVX_INCLUDES=$OPENVX_DIR/include 
      -DOPENVX_LIBRARIES=$OPENVX_DIR/bin/libopenvx.so\;$OPENVX_DIR/bin/libvxu.so\; 
      PATH_TO/openvx-samples/canny-edge-detector/
make
```
* Run the sample

```
Usage:
      ./cannyDetect --image <imageName>
      ./cannyDetect --live 
```
