cmake_minimum_required(VERSION 3.8)
project(ashioto_interfaces)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

find_package(std_msgs REQUIRED)
find_package(geometry_msgs REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/Footsteps.msg"
  "msg/Obstacle.msg"
  "msg/Point2.msg"
  "msg/Point3.msg"
  DEPENDENCIES std_msgs geometry_msgs
)
ament_export_dependencies(rosidl_default_runtime)
ament_package()
