# LiDAR-Based SLAM Robot using ROS2 Humble

A ROS2-based mobile robot simulation that performs **Simultaneous Localization and Mapping (SLAM)** using LiDAR sensor data. The project demonstrates autonomous mapping, robot localization, obstacle detection, and visualization using Gazebo and RViz2.

---

## Project Overview

This project implements a mobile robot in a simulated environment using **ROS2 Humble**. The robot uses a LiDAR sensor to scan its surroundings and create a real-time occupancy grid map using SLAM Toolbox. The simulation is performed in Gazebo, while RViz2 is used for visualization.

---

## Features

- LiDAR-based environment mapping
- Real-time SLAM using SLAM Toolbox
- TurtleBot3 simulation in Gazebo
- Robot visualization in RViz2
- Obstacle detection using LaserScan
- Velocity control using ROS2 Python node
- Occupancy Grid Map generation
- ROS2 launch file support

---

## Technologies Used

- Ubuntu 22.04
- ROS2 Humble
- Python 3
- Gazebo
- RViz2
- TurtleBot3
- SLAM Toolbox

---

## Project Structure

```
lidar_slam_ws/
└── src/
    └── lidar_slam_robot/
        ├── config/
        ├── launch/
        │   └── slam.launch.py
        ├── lidar_slam_robot/
        │   ├── __init__.py
        │   └── teleop_controller.py
        ├── maps/
        ├── resource/
        ├── screenshots/
        ├── package.xml
        ├── setup.py
        ├── setup.cfg
        └── README.md
```

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/lidar_slam_robot.git
```

### Navigate to Workspace

```bash
cd lidar_slam_ws
```

### Build the Package

```bash
colcon build
```

### Source the Workspace

```bash
source install/setup.bash
```

---

## Running the Project

### Set TurtleBot3 Model

```bash
export TURTLEBOT3_MODEL=burger
```

### Launch Gazebo

```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```

### Launch SLAM Toolbox

```bash
ros2 launch slam_toolbox online_async_launch.py
```

### Run the Robot Controller

```bash
ros2 run lidar_slam_robot teleop_controller
```

---

## Project Workflow

```
Start Simulation
        │
        ▼
Launch TurtleBot3
        │
        ▼
LiDAR Sensor
        │
        ▼
Laser Scan Data
        │
        ▼
SLAM Toolbox
        │
        ▼
Occupancy Grid Map
        │
        ▼
RViz2 Visualization
```

---

## Results

- Successfully simulated a TurtleBot3 robot in Gazebo.
- Generated real-time occupancy grid maps using LiDAR.
- Visualized robot movement and sensor data in RViz2.
- Implemented a ROS2 Python node for robot motion control.
- Demonstrated basic obstacle detection using LaserScan data.

---

## Future Improvements

- Autonomous navigation using Nav2
- Warehouse path planning
- Waypoint navigation
- Dynamic obstacle avoidance
- Multi-robot coordination
- Autonomous pick-and-place integration

---

## Screenshots

### Gazebo Simulation

> Add `screenshots/gazebo.png`

### RViz2 Visualization

> Add `screenshots/rviz.png`

---

## Contributors

This project was developed collaboratively by:

- **Harshvardhan Nayakal**
- **Sakshi Patil**

---

## License

This project is intended for educational and research purposes.
