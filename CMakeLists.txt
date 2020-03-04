cmake_minimum_required(VERSION 3.0.2)
project(protocol_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation)

add_message_files(
  DIRECTORY msg
  FILES
  Packet.msg
)

generate_messages()

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS message_runtime)
