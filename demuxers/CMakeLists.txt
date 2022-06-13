cmake_minimum_required(VERSION 3.5)

project(demuxers LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB SOURCES ./ffdemuxer/*.cpp ./ffdemuxer/*.cc)
file(GLOB HEADES ./ffdemuxer/*.h)

add_library(${PROJECT_NAME} ${SOURCES} ${HEADES})
target_link_libraries(${PROJECT_NAME} PUBLIC avutil avcodec avdevice avformat swresample)

