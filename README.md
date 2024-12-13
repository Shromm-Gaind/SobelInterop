# SobelInterop

Sobel edge detection algorithim using OpenCL, OpenCV, and OpenGL.

https://en.wikipedia.org/wiki/Sobel_operator

## Prerequisites

```bash
sudo apt update
sudo apt install -y \
    build-essential \
    cmake \
    opencl-headers \
    ocl-icd-opencl-dev \
    libopencv-dev \
    libglfw3-dev \
    libgl1-mesa-dev
```

## OpenCL Runtime Installation

Install one of the following:
- Intel: `sudo apt install intel-opencl-icd`
- AMD: `sudo apt install mesa-opencl-icd`
- NVIDIA: Install CUDA toolkit from NVIDIA website

## Build Instructions

```bash
mkdir build
cd build
cmake ..
make
```

## Run

```bash
./SobelInterop
```

## Troubleshooting

- Run `clinfo` to verify OpenCL installation
- Check GPU drivers for OpenGL issues
- Verify dependencies: `dpkg -l | grep -E 'opencl|opencv|glfw'`
