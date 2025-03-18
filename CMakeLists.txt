# CMakeLists.txt
cmake_minimum_required(VERSION 3.10)
project(helloworld)

# 设置C++标准为 C++11 或更高
set(CMAKE_CXX_STANDARD 11)

# 指定源文件
add_executable(helloworld helloworld.cpp)


# 获取当前的时间戳
string(TIMESTAMP BUILD_TIMESTAMP "%Y-%m-%d %H:%M:%S")
message(STATUS "build time is ${BUILD_TIMESTAMP}")
## 配置一个头文件，将commit号写入
configure_file(
        ${CMAKE_CURRENT_SOURCE_DIR}/version.h.in
        ${CMAKE_CURRENT_SOURCE_DIR}/version.h
        @ONLY
)


