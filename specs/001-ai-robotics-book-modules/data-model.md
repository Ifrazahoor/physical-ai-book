# Data Model: Robotic Nervous System (ROS 2)

## ROS 2 Messages

### `/joint_states` (sensor_msgs/JointState)
- **Description**: Publishes the current state of all joints.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `name`: `string[]` (names of the joints)
  - `position`: `float64[]` (current position of the joints)
  - `velocity`: `float64[]` (current velocity of the joints)
  - `effort`: `float64[]` (current effort of the joints)

### `/joint_command` (std_msgs/Float64MultiArray)
- **Description**: Subscribes to commands for the joints.
- **Fields**:
  - `layout`: `std_msgs/MultiArrayLayout`
  - `data`: `float64[]` (target positions for the joints)

## ROS 2 Services

### `/set_speed` (custom_interfaces/SetSpeed)
- **Description**: Service to set the speed of the robot's movement.
- **Request**:
  - `speed`: `float64`
- **Response**:
  - `success`: `bool`
