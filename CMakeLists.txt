cmake_minimum_required(VERSION 2.8)

project(json CXX)

add_executable(json_unit
    src/json.hpp test/catch.hpp test/unit.cpp
)

if(MSVC)
    set(CMAKE_CXX_FLAGS
        "/EHsc"
    )
else(MSVC)
    set(CMAKE_CXX_FLAGS
        "-std=c++11 -stdlib=libc++"
    )
endif(MSVC)

include_directories(
    src test
)
