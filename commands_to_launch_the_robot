##LOCALAZATION WITH SLAM##

<--TO RUN TWIST MUX AND REMAPPING OF TOPIC-->

ros2 run  twist_mux twist_mux --ros-args --params-file ./src/my_bot/config/twist_mux.yaml -r cmd_vel:=diff_cont/cmd_vel_unstamped

<--TO LAUNCH GAZEBO-->

ros2 launch my_bot launch_sim.launch.py world:=./src/my_bot/worlds/maze3world.world 

<--TO LAUNCH RVIZ-->

rviz2

<--TO LAUNCH SLAM-->

ros2 launch my_bot online_async_launch.py params_file:=./src/my_bot/config/mapper_params_online_async.yaml use_sim_time:=true

<--TO LAUNCH NAV2-->

ros2 launch my_bot navigation_launch.py use_sim_time:=true

<--TO RUN TELEOP-->

ros2 run teleop_twist_keyboard teleop_twist_keyboard



##LOCALIZATION WITH AMCL##

<--TO RUN TWIST MUX AND REMAPPING OF TOPIC-->

ros2 run  twist_mux twist_mux --ros-args --params-file ./src/my_bot/config/twist_mux.yaml -r cmd_vel:=diff_cont/cmd_vel_unstamped

<--TO LAUNCH GAZEBO-->

ros2 launch my_bot launch_sim.launch.py world:=./src/my_bot/worlds/maze3world.world 

<--TO LAUNCH RVIZ-->

rviz2

<--TO RUN AMCL-->

ros2 launch my_bot localization_launch.py map:=./maze2_world_map_save.yaml use_sim_time:=true

<--TO LAUNCH NAV2-->

ros2 launch my_bot navigation_launch.py use_sim_time:=true map_subscribe_transient_local:=true
