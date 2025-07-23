cmake_minimum_required(VERSION 3.0.2)
project(multidrone_messages)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  geometry_msgs
  message_generation
)

add_message_files(
  FILES
  Trajectory.msg
  RichTrajectory.msg
  ReplanInfo.msg
  Coefficients.msg
  TestMsg.msg
  InitMsg.msg
  ObstacleMsg.msg
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
