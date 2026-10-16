# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-09-04

### Added
- Unified URDF/Xacro model combining MiR 250 base, UR5e arm, Robotiq gripper, and RealSense D435i
- Gazebo Classic simulation with maze world environment
- SLAM Toolbox integration for 2D occupancy grid mapping
- Nav2 navigation stack with AMCL localization
- MoveIt 2 integration for UR5e arm motion planning
- ArUco marker detection and pose estimation
- Vision-guided navigation (ArUco → Nav2 goal)
- Vision-guided manipulation (ArUco → MoveIt 2 target)
- Point cloud processing utilities
- Laser scan merger (ira_laser_tools)
- Pre-built maze map for navigation demos
- Comprehensive documentation and quickstart guide

### Dependencies
- ROS 2 Humble Hawksbill
- Gazebo Classic 11
- MoveIt 2
- Nav2
- SLAM Toolbox
- Universal Robots ROS2 Driver
