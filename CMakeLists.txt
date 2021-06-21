cmake_minimum_required(VERSION 2.8.3)
project(multi_turtlebot3)

find_package(catkin REQUIRED COMPONENTS roslaunch genmsg actionlib_msgs actionlib rospy std_msgs)
find_package(geometry_msgs)

add_action_files(DIRECTORY action FILES NavigateWaypoint.action InspectWaypoint.action CheckBattery.action Charge.action)

catkin_python_setup()

generate_messages(DEPENDENCIES actionlib_msgs std_msgs geometry_msgs)

catkin_package()

roslaunch_add_file_check(launch/home_world.launch)
roslaunch_add_file_check(launch/home_world_robots.launch)
roslaunch_add_file_check(launch/battery_servers.launch)
roslaunch_add_file_check(launch/turtlebot3_bringup.launch)
roslaunch_add_file_check(launch/turtlebot3_navigation.launch)
roslaunch_add_file_check(launch/move_base.launch)
roslaunch_add_file_check(launch/amcl.launch)

install(
	DIRECTORY launch rviz config urdf
	DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
