cmake_minimum_required(VERSION 3.14)

project(QT_Net_BD LANGUAGES CXX)

set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTORCC ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(QT NAMES Qt6 Qt5 REQUIRED COMPONENTS Core Sql Network)
find_package(Qt${QT_VERSION_MAJOR} REQUIRED COMPONENTS Core Sql Network)

add_executable(QT_Net_BD
  main.cpp
)
target_link_libraries(QT_Net_BD Qt${QT_VERSION_MAJOR}::Core Qt${QT_VERSION_MAJOR}::Sql Qt${QT_VERSION_MAJOR}::Network)

install(TARGETS QT_Net_BD
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR})
