cmake_minimum_required(VERSION 3.0.2)
project(opensimrt_msgs)

find_package(catkin REQUIRED message_generation std_msgs geometry_msgs)

add_message_files(
    DIRECTORY msg
    FILES
    Common.msg
    CommonTimed.msg
    PointWrenchTimed.msg
    Labels.msg
    )

add_service_files(
    DIRECTORY srv
    FILES
    LabelsSrv.srv

)
 generate_messages(
   DEPENDENCIES
   std_msgs  
   geometry_msgs
   )

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs geometry_msgs
)

