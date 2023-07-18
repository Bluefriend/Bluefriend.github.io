![](https://blog.desdelinux.net/wp-content/uploads/2019/07/cmake.jpg){ width="400" }

## Objective
---
Build libraries or executables for cross-platform using CMake

## Platforms
---
- Windows
    - MSVC
- Linux
    - Clang
    - GCC
- Android
    - Clang (NDK)
- iOS/MacOS
    - AppleClang
- WebAssembly
    - Emscripten

## Tools
---
- MSVC build tools (Windows)
- Clang/GCC (Linux)
- Android SDK/ NDK (Android)
- Xcode (iOS/MacOS)
- Emscripten (WebAssembly)
- CMake

## Folder structure
---
- bin
- app
    - CMakeLists.txt
- cmake
    - utils.cmake
- doc
- module
    - SampleModule
      - CMakeLists.txt
- platform
    - Android
      - CMakeLists.txt
    - iOS
      - CMakeLists.txt
    - Web
      - CMakeLists.txt
- test
- resource
- CMakeLists.txt

## Features
---
- Import other dependencies if developer set the library path
- Build library or executable for exact target
- Compile unit tests files
- Detect target platform's architecture and set the SIMD
- Setup compiler flags for optimization

## Reference
---
- [CMake Documentation](https://cmake.org/cmake/help/latest/)
- [OpenCV CMake file](https://github.com/opencv/opencv/blob/master/CMakeLists.txt)