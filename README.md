# Diff-drive-robot

## How to run
- Build the package from the root of the workspace 
```bash
colcon build --symlink-install --packages-select diff_drive_robot
```

- Source the setup file
```bash
source install/setup.bash
```

- Launch the `robot_state_publisher` node
```bash
ros2 launch diff_drive_robot rsp.launch.py 
```

- Launch `joint_state_publisher_gui` 
```bash
ros2 run joint_state_publisher_gui joint_state_publisher_gui
```