# Quickstart: Robotic Nervous System (ROS 2)

This quickstart guide will help you get the ROS 2 environment up and running for the "Robotic Nervous System" module.

## Prerequisites

- Docker installed on your system.

## Running the Docker Container

1.  **Build the Docker image**:
    ```bash
    cd src/docker
    docker build -t ros2-humble-dev .
    ```

2.  **Run the Docker container**:
    ```bash
    docker run -it --rm -v ./src/ros2_ws:/ros2_ws ros2-humble-dev
    ```

## Building the ROS 2 Workspace

Inside the Docker container:

1.  **Source the ROS 2 setup file**:
    ```bash
    source /opt/ros/humble/setup.bash
    ```

2.  **Build the workspace**:
    ```bash
    cd /ros2_ws
    colcon build
    ```

## Running the Joint Controller

1.  **Source the workspace setup file**:
    ```bash
    source /ros2_ws/install/setup.bash
    ```

2.  **Launch the joint controller**:
    ```bash
    ros2 launch humanoid_control joint_controller.launch.py
    ```
