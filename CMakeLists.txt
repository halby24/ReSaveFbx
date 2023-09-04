SET(CMAKE_MIN_REQ_VERSION 2.4)
cmake_minimum_required(VERSION ${CMAKE_MIN_REQ_VERSION})
SET(FBX_ROOT "C:/Program Files/Autodesk/FBX/FBX SDK/2020.3.4")
INCLUDE("CMakeSettings.txt")

FBX_PROJECT(ReSaveFbx .)
SET(FBX_TARGET_SOURCE
    src/main.cxx
    src/Common.h
    src/Common.cxx
)
ADD_EXECUTABLE(
   ${FBX_TARGET_NAME}
   ${FBX_TARGET_SOURCE}
)
SET_SAMPLES_GLOBAL_FLAGS()
