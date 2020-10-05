cmake_minimum_required(VERSION 3.5)

project(string_publisher LANGUAGES C)

find_package(ament_cmake REQUIRED)
find_package(rcl REQUIRED)
find_package(rclc REQUIRED)
find_package(std_msgs REQUIRED)
find_package(rmw_zenoh_cpp REQUIRED)

add_executable(${PROJECT_NAME} main.c)

ament_target_dependencies(${PROJECT_NAME}
  rcl
  rclc
  std_msgs
  rmw_zenoh_cpp
  )

install(TARGETS ${PROJECT_NAME}
  DESTINATION ${PROJECT_NAME}
  )
