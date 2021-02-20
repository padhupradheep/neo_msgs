cmake_minimum_required(VERSION 3.5)
project(neo_msgs)

## By default build with code optimization and no debug info
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()
if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(rosidl_generate_interfaces
  "msg/EmergencyStopState.msg"
  "msg/Keypad.msg"
  "msg/LCDOutput.msg"
  "msg/USBoard.msg"
  "msg/USBoardV2.msg"
  "msg/IOBoard.msg"
)

ament_package()


