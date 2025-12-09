# Quickstart: The AI-Robot Brain: NVIDIA Isaac™ Simulation & Humanoid Navigation

This quickstart guide will help you get the NVIDIA Isaac Sim environment with Isaac ROS and Nav2 for humanoid navigation up and running.

## Prerequisites

- NVIDIA GPU (RTX 2060 or better recommended).
- NVIDIA Isaac Sim 2023.1.1 or later installed.
- Docker and NVIDIA Container Toolkit installed.

## Setting Up Isaac Sim

1.  **Launch Isaac Sim**:
    Follow the official Isaac Sim documentation to launch the Omniverse Launcher and then Isaac Sim.

2.  **Open Project**:
    Navigate to the `isaac_sim_projects/humanoid_navigation` directory within Isaac Sim to open the project.

3.  **Run Simulation**:
    In Isaac Sim, open the `humanoid_navigation.usd` scene and press the Play button to start the simulation.

## Setting Up Isaac ROS & Nav2 Environment (Docker)

1.  **Build the Docker image**:
    (Assuming you have a Dockerfile in `src/ros2_ws/docker/Dockerfile` that includes Isaac ROS Humble and Nav2)
    ```bash
    cd src/ros2_ws/docker
    docker build -t isaac-ros-nav2-env .
    ```

2.  **Run the Docker container**:
    ```bash
    docker run -it --rm --privileged --net=host --ipc=host -e "DISPLAY=$DISPLAY" -v /tmp/.X11-unix:/tmp/.X11-unix -v ./src/ros2_ws:/ros2_ws isaac-ros-nav2-env
    ```

## Running Isaac ROS & Nav2

Inside the Docker container:

1.  **Source ROS 2 setup**:
    ```bash
    source /opt/ros/humble/setup.bash
    ```

2.  **Build ROS 2 workspace**:
    ```bash
    cd /ros2_ws
    colcon build
    ```

3.  **Launch VSLAM and Navigation**:
    ```bash
    ros2 launch nav2_humanoid_bringup bringup_launch.py
    ```
    (Ensure Isaac Sim is running and publishing required topics for VSLAM and navigation.)
