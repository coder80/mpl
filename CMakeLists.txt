cmake_minimum_required(VERSION 3.5)

project(mpl LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(demuxers)

file(GLOB SOURCES ./*.cpp ./*.cc)
file(GLOB HEADES ./*.h)

add_executable(${PROJECT_NAME} ${SOURCES} ${HEADES})
target_link_libraries(${PROJECT_NAME} PUBLIC demuxers)
