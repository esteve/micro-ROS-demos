cmake_minimum_required(VERSION 3.5)

project(complex_msg_publisher LANGUAGES C)

find_package(ament_cmake REQUIRED)
find_package(rcl REQUIRED)
find_package(rclc REQUIRED)
find_package(complex_msgs REQUIRED)
find_package(rmw_microxrcedds REQUIRED)

add_executable(${PROJECT_NAME} main.c)

ament_target_dependencies(${PROJECT_NAME}
  rcl
  rclc
  complex_msgs
  rmw_microxrcedds
  )

install(TARGETS ${PROJECT_NAME}
  DESTINATION ${PROJECT_NAME}
  )
