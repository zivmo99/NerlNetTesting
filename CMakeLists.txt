cmake_minimum_required(VERSION 3.17)
project(NErlNet)

set(CMAKE_CXX_STANDARD 14)

include_directories(src_cpp/cppBridge)
include_directories(src_cpp/cppBridge/include)
include_directories(src_cpp/cppSANN)
include_directories(src_erl)

add_executable(NErlNet
        src_cpp/cppBridge/include/nifpp.h
        src_cpp/cppBridge/NerlNIF.cpp
        src_erl/erlBridge/erlModule.erl
        src_erl/erlBridge/nerlNetStatem.erl
        src_erl/erlBridge/parse.erl
        src_erl/erlBridge/startMod.erl
        src_py/BuildScript.py
        src_py/SConstruct
        build.sh
        LICENSE
        nerlnet_log_large.jpg
        Nerlnet_logo.jpg
        README.md)
