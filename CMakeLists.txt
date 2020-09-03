cmake_minimum_required(VERSION 3.16)
project(curl_sample)

set(CMAKE_CXX_STANDARD 11)

set(LIBCURL_ROOT "/usr/local")

include_directories(${LIBCURL_ROOT}/include)

link_directories(${LIBCURL_ROOT}/lib)

add_executable(curl_sample main.cpp
        mycurl/HttpImpl.cpp)

#添加链接库
target_link_libraries(curl_sample libcurl.a)