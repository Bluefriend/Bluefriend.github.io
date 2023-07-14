![](https://blog.desdelinux.net/wp-content/uploads/2019/07/cmake.jpg){ width="400" }

[CMAKE](https://cmake.org/)는 하나의 스크립트 파일로 크로스 플랫폼에 대해 컴파일을 지원하는 도구

## Objective
---
CMake를 이용하여 C++로 작성되어 있는 모듈을 각 플랫폼에서 실행 가능한 바이너리 또는 라이브러리 형태로 빌드하는 것

## Cross platform
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
- resource
- CMakeLists.txt

## Flow
---
1. Root 상에 있는 CMakeLists.txt에 프로젝트에 대한 기본적인 설정들(버전, 이름, C++ 버전 등)을 설정하고 각 플랫폼마다 공유할 수 있는 플래그들을 설정
2. CMake에서 타겟 플랫폼에 대한 정보를 추출한 뒤에 해당 플랫폼에 대한 하위 CMake들을 포함
3. Platform 폴더에 있는 CMake에서 타겟 플랫폼을 위한 플래그 설정
4. Platform 폴더에서 빌드 한 라이브러리를 app에서 참조 하도록 설정
5. 각각의 빌드 순서는 Depends를 이용하여 구성

## Reference
---
- [CMake Documentation](https://cmake.org/cmake/help/latest/)
- [OpenCV CMake file](https://github.com/opencv/opencv/blob/master/CMakeLists.txt)