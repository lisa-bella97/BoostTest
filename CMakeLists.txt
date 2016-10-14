cmake_minimum_required(VERSION 2.8.7)
project(BoostTest)

set(Boost_USE_STATIC_LIBS ON)
set(Boost_USE_MULTITHREADED ON)
set(Boost_USE_STATIC_RUNTIME OFF)
find_package(Boost COMPONENTS regex REQUIRED)

if(Boost_FOUND)
  include_directories(${Boost_INCLUDE_DIRS})
  add_executable(BoostTest main.cpp)
  target_link_libraries(BoostTest ${Boost_LIBRARIES})
endif()
