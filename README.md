For running the Goliath with slam, for mapping the surrounding for the first time.
If it is a simulation, use the world_name as "small_house".

Use
```
ros2 launch goliath_bringup simulation.launch.py world_name:=small_house use_slam:=true
```

For using it without SLAM i.e. The Nav2 stack starts working:

Use
```
ros2 launch goliath_bringup simulation.launch.py world_name:=small_house use_slam:=false
```

Manual moving of the robot can be done using either of the following two commands

```
ros2 run key_teleop key_teleop
```
OR

```
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -p stamped:=false -r cmd_vel:=amr_controller/cmd_vel_unstamped
```

Simultaneously, it can also run Moveit2 using the following command:

```
ros2 launch goliath_moveit moveit.launch.py
```
