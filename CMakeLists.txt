cmake_minimum_required(VERSION 3.20)

project(noise-canceling CXX)

find_package(portaudio REQUIRED)

add_executable(noise-canceling src/main.cpp)
target_link_libraries(video-to-sound portaudio)

target_include_directories(video-to-sound PUBLIC ${portaudio_INCLUDE_DIRS})
