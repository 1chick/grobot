cmake_minimum_required(VERSION 2.8.3)
project(grobot_msgs)

find_package(catkin REQUIRED COMPONENTS std_msgs uuid_msgs geometry_msgs std_srvs message_generation)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  VoiceLocalsEntry.msg
)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  AddPosition.srv
  DeletePosition.srv
  GetAllPosition.srv
  ModifyPosition.srv
  ResetAllPosition.srv
  SavePosition.srv
)

generate_messages(DEPENDENCIES std_msgs uuid_msgs geometry_msgs)

catkin_package(CATKIN_DEPENDS std_msgs uuid_msgs geometry_msgs std_srvs message_runtime)
