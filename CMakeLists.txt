# http://ros.org/doc/groovy/api/catkin/html/user_guide/supposed.html
cmake_minimum_required(VERSION 2.8.3)
project(robotiq_s_model_visualization)

set(CMAKE_BUILD_TYPE Release)
set(CMAKE_CXX_FLAGS "-std=c++0x")
add_definitions(-DROS)

find_package(catkin REQUIRED COMPONENTS urdf)
catkin_package(
    INCLUDE_DIRS
      cfg
      meshes
    CATKIN_DEPENDS
      urdf
    LIBRARIES
      ${PROJECT_NAME}
)
install(DIRECTORY cfg DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY meshes DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
