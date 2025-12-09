# Research: The Digital Twin: Gazebo & Unity Simulation

## Gazebo Physics Simulation
- **Decision**: Leverage SDF (Simulation Description Format) for defining robot models and environments in Gazebo.
- **Rationale**: SDF is the native format for Gazebo, providing comprehensive capabilities for physics, sensors, and plugins.
- **Alternatives considered**: URDF (Unified Robot Description Format) - less comprehensive for environment descriptions.

## Unity Rendering & Human-Robot Interaction
- **Decision**: Utilize Unity's High Definition Render Pipeline (HDRP) or Universal Render Pipeline (URP) for high-fidelity rendering.
- **Rationale**: These pipelines offer advanced graphics features necessary for realistic visual environments and human-robot interaction.
- **Alternatives considered**: Standard Render Pipeline - lacks visual quality for this project's goals.

## Sensor Modeling (LiDAR, Depth Cameras, IMUs)
- **Decision**: Implement custom Unity scripts for sensor data generation, possibly integrating with existing ROS 2 bridges (e.g., Unity-ROS-TCP-Connector).
- **Rationale**: Custom scripts allow for fine-grained control over sensor parameters and noise models, ensuring accuracy and reproducibility. ROS 2 bridges facilitate data transfer to Gazebo or external ROS nodes.
- **Alternatives considered**: Pre-built Unity assets - may lack customization or integration with ROS 2.
