cmake_minimum_required(VERSION 2.8.3)
project(sailbot_msg)

find_package(catkin REQUIRED COMPONENTS
  std_msgs
  message_generation
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  AISMsg.msg
  AISShip.msg
  GPS.msg
  heading.msg
  latlon.msg
  path.msg
  windSensor.msg
  Sensors.msg
  globalWind.msg
  addBoat.msg
  actuation_angle.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
