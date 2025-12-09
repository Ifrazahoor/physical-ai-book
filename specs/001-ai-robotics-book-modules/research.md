# Research: Robotic Nervous System (ROS 2)

**Decision**: Use ROS 2 Humble Hawksbill.
**Rationale**: ROS 2 Humble is the latest long-term support (LTS) release, ensuring stability and long-term availability of packages and documentation.

**Decision**: Use `rclpy` for Python integration.
**Rationale**: `rclpy` is the official and most widely used Python client library for ROS 2. It provides a complete and well-documented API for interacting with ROS 2.

**Decision**: Use URDF for robot modeling.
**Rationale**: URDF is the standard format for representing robot models in ROS. It is well-supported by ROS tools like Gazebo and RViz.

**Decision**: Use Docker for containerization.
**Rationale**: Docker provides a lightweight and reproducible way to package the ROS 2 environment and all its dependencies, ensuring that students can run the examples on any platform.
