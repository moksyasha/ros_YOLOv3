################################################################################
# Set minimum required version of cmake, project name and compile options
################################################################################
cmake_minimum_required(VERSION 3.0.2)
project(driving)

################################################################################
# Find catkin packages and libraries for catkin and system dependencies
################################################################################
find_package(catkin REQUIRED COMPONENTS
  turtlebot3_autorace_msgs
  dynamic_reconfigure
)
################################################################################
# Setup for python modules and scripts
################################################################################
catkin_python_setup()

################################################################################
# Declare ROS messages, services and actions
################################################################################

################################################################################
# Declare ROS dynamic reconfigure parameters
################################################################################

#add dynamic reconfigure api
#find_package(catkin REQUIRED dynamic_reconfigure)
generate_dynamic_reconfigure_options(
  cfg/dynamic.cfg
  #...
)

# make sure configure headers are built before any node using them
#add_dependencies(control_lane $driving_gencfg)

################################################################################
# Declare catkin specific configuration to be passed to dependent projects
################################################################################
catkin_package(
  CATKIN_DEPENDS turtlebot3_autorace_msgs
)
################################################################################
# Build
################################################################################

################################################################################
# Install
################################################################################
catkin_install_python(PROGRAMS
  nodes/control_lane
  nodes/constr
  nodes/tunnel
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY launch
	DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)



################################################################################
# Test
################################################################################

