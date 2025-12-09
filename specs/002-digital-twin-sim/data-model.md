# Data Model: The Digital Twin: Gazebo & Unity Simulation

## Sensor Data Messages (for ROS 2 Integration)

### LiDAR Data (sensor_msgs/LaserScan)
- **Description**: Represents a single scan from a LiDAR sensor.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `angle_min`: `float32` (start angle of the scan [rad])
  - `angle_max`: `float32` (end angle of the scan [rad])
  - `angle_increment`: `float32` (angular distance between measurements [rad])
  - `time_increment`: `float32` (time between measurements [seconds])
  - `scan_time`: `float32` (time between scans [seconds])
  - `range_min`: `float32` (minimum range value [m])
  - `range_max`: `float32` (maximum range value [m])
  - `ranges`: `float32[]` (range data [m])
  - `intensities`: `float32[]` (intensity data)

### Depth Camera Data (sensor_msgs/Image and sensor_msgs/CameraInfo)
- **Description**: Image data from a depth camera.
- **Image Fields**:
  - `header`: `std_msgs/Header`
  - `height`: `uint32` (image height)
  - `width`: `uint32` (image width)
  - `encoding`: `string` (encoding format, e.g., "16UC1" for 16-bit unsigned depth)
  - `is_bigendian`: `uint8`
  - `step`: `uint32` (full row length in bytes)
  - `data`: `uint8[]` (raw image data)
- **CameraInfo Fields**:
  - `header`: `std_msgs/Header`
  - `height`: `uint32`
  - `width`: `uint32`
  - `K`: `float64[9]` (intrinsic camera matrix)
  - `D`: `float64[]` (distortion coefficients)
  - ... (other camera parameters)

### IMU Data (sensor_msgs/Imu)
- **Description**: Data from an Inertial Measurement Unit.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `orientation`: `geometry_msgs/Quaternion` (quaternion representing orientation)
  - `angular_velocity`: `geometry_msgs/Vector3`
  - `linear_acceleration`: `geometry_msgs/Vector3`
  - `orientation_covariance`: `float64[9]`
  - `angular_velocity_covariance`: `float64[9]`
  - `linear_acceleration_covariance`: `float64[9]`

## Humanoid Robot State (custom message)

### `humanoid_msgs/HumanoidState`
- **Description**: Custom message to represent the full state of the humanoid robot.
- **Fields**:
  - `header`: `std_msgs/Header`
  - `joint_positions`: `float64[]`
  - `joint_velocities`: `float64[]`
  - `joint_efforts`: `float64[]`
  - `base_pose`: `geometry_msgs/Pose` (position and orientation of the robot's base)
  - `base_velocity`: `geometry_msgs/Twist` (linear and angular velocity of the robot's base)
