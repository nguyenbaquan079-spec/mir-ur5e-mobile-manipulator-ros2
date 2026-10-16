# Contributing to MiR-UR5e Mobile Manipulator

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to this project.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)

## Code of Conduct

This project follows the [ROS Community Code of Conduct](https://www.ros.org/code-of-conduct/). Please be respectful and constructive in all interactions.

## How Can I Contribute?

### 🐛 Report Bugs

- Use [GitHub Issues](https://github.com/nguyenbaquan079-spec/mir-ur5e-mobile-manipulator-ros2/issues) to report bugs
- Include your ROS 2 version, Ubuntu version, and Gazebo version
- Provide steps to reproduce the issue
- Include relevant log output

### 💡 Suggest Features

- Open a [GitHub Issue](https://github.com/nguyenbaquan079-spec/mir-ur5e-mobile-manipulator-ros2/issues) with the `enhancement` label
- Describe the feature and its use case
- If possible, include a proposed implementation approach

### 🔧 Submit Code

1. Fork the repository
2. Create a feature branch from `main`
3. Make your changes
4. Test thoroughly
5. Submit a Pull Request

## Development Setup

```bash
# Clone your fork
git clone https://github.com/<your-username>/mir-ur5e-mobile-manipulator-ros2.git src/mir_robot
cd ~/ros2_ws

# Install dependencies
rosdep install --from-paths src --ignore-src -r -y

# Build with debug symbols
colcon build --cmake-args -DCMAKE_BUILD_TYPE=Debug
```

## Coding Standards

### C++
- Follow the [ROS 2 C++ Style Guide](https://docs.ros.org/en/humble/The-ROS2-Project/Contributing/Code-Style-Language-Versions.html)
- Use `clang-format` with the provided `.clang-format` config
- Include appropriate comments and documentation

### Python
- Follow [PEP 8](https://peps.python.org/pep-0008/)
- Use type hints where possible
- Include docstrings for all public functions and classes

### Launch Files
- Use Python-based launch files (`.launch.py`)
- Document all launch arguments
- Use `DeclareLaunchArgument` for configurable parameters

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
<type>(<scope>): <description>

[optional body]

[optional footer(s)]
```

**Types:** `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`, `ci`

**Examples:**
```
feat(navigation): add dynamic obstacle avoidance
fix(moveit): resolve trajectory execution timeout
docs(readme): update installation instructions
```

## Pull Request Process

1. Update the README.md if your changes affect usage
2. Ensure all tests pass: `colcon test`
3. Update documentation as needed
4. Request review from at least one maintainer
5. Squash commits before merging if requested
