cmake_minimum_required(VERSION 3.8)
add_compile_options(-std=c++17)
project(acomms_msgs)

set(CMAKE_CXX_STANDARD 17)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  message_generation
  std_msgs
  geometry_msgs
  geographic_msgs

)

add_message_files(
  FILES
  UsblData.msg
  AcommsTx.msg
  AcommsRx.msg
  AcommsTxByteArray.msg
  AcommsRxByteArray.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  # INCLUDE_DIRS 
  # LIBRARIES
  CATKIN_DEPENDS message_runtime
  # DEPENDS
)