# Tasks: The Digital Twin: Gazebo & Unity Simulation

**Input**: Design documents from `/specs/002-digital-twin-sim/`

## Phase 1: Setup (Shared Infrastructure)

- [ ] T001 Create the base directory structure for Gazebo simulations in `src/gazebo_sims/`.
- [ ] T002 Create the base directory structure for the Unity project in `src/unity_project/`.
- [ ] T003 Create a basic Dockerfile for a Gazebo simulation environment in `src/gazebo_sims/docker/Dockerfile`.
- [ ] T004 Initialize a new Unity 2023 LTS project in `src/unity_project/`.

---

## Phase 2: Foundational (Blocking Prerequisites)

- [ ] T005 Create `simple_physics.world` for basic Gazebo physics validation in `src/gazebo_sims/worlds/`.
- [ ] T006 Create a basic 3D model (e.g., a cube) and its SDF definition for Gazebo in `src/gazebo_sims/models/basic_object/`.
- [ ] T007 Set up a new Unity Scene `HumanoidInteraction.unity` for human-robot interaction in `src/unity_project/Assets/Scenes/`.
- [ ] T008 Implement basic Unity scripts to load and display a humanoid robot model.

---

## Phase 3: User Story 1 - Understand Basic Physics Simulations in Gazebo (Priority: P1) 🎯 MVP

**Goal**: Students can understand concepts like gravity and collisions through Gazebo simulations.

**Independent Test**: Students can launch a Gazebo simulation with a simple object, observe it falling under gravity, and verify collisions with other static objects.

### Implementation for User Story 1

- [ ] T009 [US1] Validate gravity and collision physics for `basic_object` in `src/gazebo_sims/worlds/simple_physics.world`.
- [ ] T010 [US1] Develop an exercise to demonstrate object interaction in `src/gazebo_sims/worlds/object_interaction.world`.
- [ ] T011 [US1] Write Docusaurus markdown for Gazebo physics simulation concepts in `src/docusaurus/docs/gazebo-physics.md`.
- [ ] T012 [US1] Create diagrams explaining Gazebo physics and collision detection.

---

## Phase 4: User Story 2 - Create and Interact with a Unity Human-Robot Environment (Priority: P2)

**Goal**: Students can learn about high-fidelity rendering and human-robot interaction in Unity.

**Independent Test**: Students can launch a Unity simulation, observe a high-fidelity robot model, and manipulate it or interact with a human avatar within the environment.

### Implementation for User Story 2

- [ ] T013 [US2] Import or create a high-fidelity humanoid robot model into `src/unity_project/Assets/Models/`.
- [ ] T014 [US2] Implement scripts for basic human-robot interaction (e.g., joint manipulation) in `src/unity_project/Assets/Scripts/`.
- [ ] T015 [US2] Create exercises for human-robot interaction in the Unity environment.
- [ ] T016 [US2] Write Docusaurus markdown for Unity rendering and interaction in `src/docusaurus/docs/unity-rendering-interaction.md`.
- [ ] T017 [US2] Create diagrams for Unity scene setup and interaction flow.

---

## Phase 5: User Story 3 - Integrate and Interpret Simulated Sensor Data (Priority: P3)

**Goal**: Students can understand sensor modeling and data acquisition through simulated sensors in Unity.

**Independent Test**: Students can integrate simulated LiDAR, Depth Camera, and IMU sensors into their Unity environment and visualize or log their respective data outputs.

### Implementation for User Story 3

- [ ] T018 [US3] Develop a Unity script for a simulated LiDAR sensor (publisher) in `src/unity_project/Assets/Scripts/SensorPublisher.cs`.
- [ ] T019 [US3] Create a Unity Prefab for the LiDAR sensor with proper visualization in `src/unity_project/Assets/Sensors/LiDAR.prefab`.
- [ ] T020 [US3] Develop a Unity script for a simulated Depth Camera (publisher) in `src/unity_project/Assets/Scripts/SensorPublisher.cs`.
- [ ] T021 [US3] Create a Unity Prefab for the Depth Camera with proper visualization in `src/unity_project/Assets/Sensors/DepthCamera.prefab`.
- [ ] T022 [US3] Develop a Unity script for a simulated IMU (publisher) in `src/unity_project/Assets/Scripts/SensorPublisher.cs`.
- [ ] T023 [US3] Create a Unity Prefab for the IMU sensor in `src/unity_project/Assets/Sensors/IMU.prefab`.
- [ ] T024 [US3] Implement data visualization and interpretation exercises for each sensor in the Unity environment.
- [ ] T025 [US3] Write Docusaurus markdown for simulated sensor integration and data interpretation in `src/docusaurus/docs/sensor-integration.md`.
- [ ] T026 [US3] Create diagrams illustrating sensor data output and coordinate frames.

---

## Phase N: Polish & Cross-Cutting Concerns

- [ ] T027 Review and refactor all simulation code and Unity scripts.
- [ ] T028 Validate all exercises and diagrams for accuracy and clarity.
- [ ] T029 Ensure Docusaurus compatibility and successful build for all new content.
- [ ] T030 Verify reproducibility of all environments using Docker.
