set(CMAKE_SYSTEM_PREFIX_PATH "/home/user/Qt/5.15.2/gcc_64")
cmake_minimum_required(VERSION 3.0.0)
project(jen-cpp VERSION 0.1.0)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

include(CTest)
enable_testing()
find_package(Qt5 REQUIRED COMPONENTS Widgets Multimedia MultimediaWidgets OpenGL Quick Qml) 

add_executable(jen-cpp source/main.cpp source/resources.qrc)
target_link_libraries(jen-cpp Qt5::Widgets Qt5::Multimedia Qt5::MultimediaWidgets Qt5::Quick Qt5::OpenGL Qt5::Qml)

