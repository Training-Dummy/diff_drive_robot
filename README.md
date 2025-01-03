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

## View URDF in RViz
- Launch RViz in a separate terminal
```bash
rviz2
```
- Configure RViz settings
    - Set fixed frame to `world`
    - Select "Add", then click `RobotModel` display
        - Set the topic to `/robot_description`
        - Set alpha to 0.8
    - Select "Add", then click `TF` display
        - Enable names

- Save RViz configuration
    - File → save as → navigate to config folder and save the file (e.g. `config/diff-drive.rviz`)

- Run Rviz with saved configuration file
```bash
rviz2 -d src/diff_drive_robot/config/diff-drive.rviz
```