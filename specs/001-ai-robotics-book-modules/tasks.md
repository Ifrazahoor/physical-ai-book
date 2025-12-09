# Tasks: Robotic Nervous System (ROS 2)

**Input**: Design documents from `/specs/001-ai-robotics-book-modules/`

## Phase 1: Setup (Shared Infrastructure)

- [ ] T001 Create project structure for the ROS 2 workspace at `src/ros2_ws/src/humanoid_control`.
- [ ] T002 Create a `package.xml` file for the `humanoid_control` package in `src/ros2_ws/src/humanoid_control`.
- [ ] T003 Create a `setup.py` file for the `humanoid_control` package in `src/ros2_ws/src/humanoid_control`.
- [ ] T004 Create a Dockerfile for the ROS 2 environment in `src/docker/Dockerfile`.

---

## Phase 2: Foundational (Blocking Prerequisites)

- [ ] T005 Implement the basic URDF model for the humanoid robot in `src/ros2_ws/src/humanoid_control/humanoid_control/urdf/humanoid.urdf`.
- [ ] T006 Create the main launch file for the `humanoid_control` package in `src/ros2_ws/src/humanoid_control/launch/joint_controller.launch.py`.

---

## Phase 3: User Story 1 - Understand and Implement ROS 2 (Priority: P1) 🎯 MVP

**Goal**: Students can control a robot's joints and understand the middleware flow.

**Independent Test**: Students can run the provided code to control a simulated robot's joints and can explain the flow of messages between nodes.

### Implementation for User Story 1

- [ ] T007 [US1] Implement a ROS 2 node that publishes joint states in `src/ros2_ws/src/humanoid_control/humanoid_control/joint_state_publisher.py`.
- [ ] T008 [US1] Implement a ROS 2 node that subscribes to joint commands and moves the robot in `src/ros2_ws/src/humanoid_control/humanoid_control/joint_controller.py`.
- [ ] T009 [US1] Implement the `SetSpeed` service server in `src/ros2_ws/src/humanoid_control/humanoid_control/set_speed_service.py`.
- [ ] T010 [US1] Create the custom service interface `custom_interfaces/SetSpeed` in `src/ros2_ws/src/humanoid_control/custom_interfaces/srv/SetSpeed.srv`.
- [ ] T011 [US1] Write a test script to verify the `SetSpeed` service in `src/ros2_ws/src/humanoid_control/test/test_set_speed.py`.
- [ ] T012 [US1] Write the Docusaurus documentation for ROS 2 concepts in `src/docusaurus/docs/module1-ros2.md`.
- [ ] T013 [US1] Add diagrams for ROS 2 Node-Topic-Service flow and URDF joint-link structure to the documentation.

---

## Phase 4: User Story 2 - Simulate a Humanoid Robot (Priority: P2)

**Goal**: Students can build and interact with a simulated humanoid robot in Gazebo and Unity.

**Independent Test**: Students can launch the Gazebo and Unity simulations and see the robot model with sensor data.

### Implementation for User Story 2

- [ ] T014 [US2] Create a Gazebo world file for the humanoid robot simulation in `src/ros2_ws/src/humanoid_control/worlds/humanoid.world`.
- [ ] T015 [US2] Create a launch file to start the Gazebo simulation in `src/ros2_ws/src/humanoid_control/launch/gazebo.launch.py`.
- [ ] T016 [US2] Integrate the robot's URDF with the Gazebo simulation.
- [ ] T017 [US2] Create a Unity project for the humanoid robot simulation.
- [ ] T018 [US2] Implement sensor visualization (LiDAR, IMU, depth cameras) in the Unity environment.
- [ ] T019 [US2] Write the Docusaurus documentation for Gazebo and Unity simulation in `src/docusaurus/docs/module2-simulation.md`.

---

## Phase 5: User Story 3 - Implement Autonomous Navigation (Priority: P3)

**Goal**: Students can implement advanced perception and navigation for a humanoid robot.

**Independent Test**: The simulated robot can navigate from a starting point to a goal point in a simulated environment with obstacles.

### Implementation for User Story 3

- [ ] T020 [US3] Set up an NVIDIA Isaac Sim project for the humanoid robot.
- [ ] T021 [US3] Implement VSLAM using Isaac ROS in the Isaac Sim environment.
- [ ] T022 [US3] Integrate Nav2 for path planning in the Isaac Sim environment.
- [ ] T023 [US3] Create a test scenario with obstacles for the robot to navigate.
- [ ] T024 [US3] Write the Docusaurus documentation for Isaac Sim and Nav2 in `src/docusaurus/docs/module3-navigation.md`.

---

## Phase N: Polish & Cross-Cutting Concerns

- [ ] T025 Review and refactor all code for clarity and efficiency.
- [ ] T026 Validate all code examples and exercises.
- [ ] T027 Ensure all documentation is complete and accurate.
