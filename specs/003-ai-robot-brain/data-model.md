# Data Model: The AI-Robot Brain: NVIDIA Isaac™ Simulation & Humanoid Navigation

## VSLAM Map Data

### `nav_msgs/OccupancyGrid`
- **Description**: Represents a 2D occupancy grid map, commonly used in VSLAM.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `info`: `nav_msgs/MapMetaData`
  - `data`: `int8[]` (The map data, in row-major order, and values from -1 to 100)

### `nav_msgs/MapMetaData`
- **Description**: Meta-data for the 2D map.
- **Fields**:
  - `map_load_time`: `builtin_interfaces/Time`
  - `resolution`: `float32` (Resolution of the map, [m/cell])
  - `width`: `uint32` (Map width, [cells])
  - `height`: `uint32` (Map height, [cells])
  - `origin`: `geometry_msgs/Pose` (The origin of the map [m, m, rad]. This is the pose of the coordinate frame of the map in relation to the coordinate frame of the world.)

## Navigation Goal

### `geometry_msgs/PoseStamped`
- **Description**: Represents a pose with reference coordinate frame and timestamp.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `pose`: `geometry_msgs/Pose`

## Humanoid Robot State

### `humanoid_msgs/HumanoidState` (Custom message - from Module 1/2)
- **Description**: Full state of the humanoid robot (position, velocity, effort of joints, base pose, base velocity).
- **Fields**:
  - `header`: `std_msgs/Header`
  - `joint_positions`: `float64[]`
  - `joint_velocities`: `float64[]`
  - `joint_efforts`: `float64[]`
  - `base_pose`: `geometry_msgs/Pose`
  - `base_velocity`: `geometry_msgs/Twist`

## Path Planning

### `nav_msgs/Path`
- **Description**: Represents a sequence of poses that make up a path.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `poses`: `geometry_msgs/PoseStamped[]`
