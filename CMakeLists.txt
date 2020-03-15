cmake_minimum_required(VERSION 3.0)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++2a")

project(lims)

#add_executable(
#  lims
#  main.cpp
#  Subscriber.cpp
#  Book.cpp
#  Borrow.cpp
#  Library.cpp
#  Title.cpp
#  )

#Bring the headers, such as Student.h into the project
include_directories(inc)

#Can manually add the sources using the set command as follows:
#set(SOURCES src/mainapp.cpp src/Student.cpp)

#However, the file(GLOB...) allows for wildcard additions:
file(GLOB SOURCES "src/*.cpp")

add_executable(lims ${SOURCES})

