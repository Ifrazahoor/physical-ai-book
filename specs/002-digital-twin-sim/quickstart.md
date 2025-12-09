# Quickstart: The Digital Twin: Gazebo & Unity Simulation

This quickstart guide will help you get the Gazebo and Unity simulation environments up and running for "The Digital Twin" module.

## Prerequisites

- Docker installed on your system.
- Unity Hub and Unity 2023 LTS installed (for Unity project development).

## Running Gazebo Simulation

1.  **Build the Gazebo Docker image**:
    (Assuming you have a Dockerfile in `src/gazebo_sims/docker/Dockerfile`)
    ```bash
    cd src/gazebo_sims/docker
    docker build -t gazebo-sim-env .
    ```

2.  **Run the Gazebo container**:
    ```bash
    docker run -it --rm -v ./src/gazebo_sims:/gazebo_ws gazebo-sim-env
    ```

3.  **Launch a Gazebo world (inside container)**:
    ```bash
    gazebo /gazebo_ws/worlds/simple_physics.world
    ```

## Setting Up Unity Project

1.  **Open Unity Hub**:
    Launch Unity Hub and add the `src/unity_project` folder as a new project.

2.  **Open Project in Unity Editor**:
    Open the `unity_project` in the Unity Editor with Unity 2023 LTS.

3.  **Load Scene**:
    Navigate to `Assets/Scenes/HumanoidInteraction.unity` and open the scene.

4.  **Run Simulation**:
    Press the Play button in the Unity Editor to start the simulation.

## Building Unity Project (for reproducible runtime)

1.  **Build from Unity Editor**:
    Go to `File > Build Settings`, select your target platform (e.g., Windows, Linux), and click `Build`.
    (Alternatively, a Dockerfile for building the Unity project could be provided in `src/unity_project/Dockerfile`).
