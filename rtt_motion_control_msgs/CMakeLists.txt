cmake_minimum_required(VERSION 3.5)
project(rtt_motion_control_msgs)

# find_package(Boost REQUIRED COMPONENTS
#   program_options
# )

find_package(ament_cmake REQUIRED)
find_package(rtt_ros2_interfaces REQUIRED)

# generate typekit
rtt_ros2_generate_interfaces_plugins(motion_control_msgs)

ament_package()

# orocos_generate_package() is deprecated for ROS 2.
# Prefer cmake target export and import instead, in combination with
# ament_export_interfaces() or ament_export_targets() when building with
# ament_cmake.
orocos_generate_package(
  DEPENDS_TARGETS rtt_ros2_interfaces
)
