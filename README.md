# Multi-Turtlebot3 Simulator using Gazebo ROS Noetic
Here you find launch files to launch multiple turtlebot3 in Gazebo.
It uses turtlebot3 packages to run.
Turtlebot3 ROS documentation can be found [here](https://emanual.robotis.com/docs/en/platform/turtlebot3/overview/).

# Setup
Install turtlebot3 dependencies as explained [here](https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/#pc-setup) and turtlebot3 simulation as explained [here](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#gazebo-simulation):

```sh
roscd
```

```sh
git clone https://github.com/cazevedo/battery_mockup.git
```

```sh
git clone https://github.com/cazevedo/cpr_gazebo.git
```

```sh
git clone https://github.com/cazevedo/robot_state_publisher2.git
```

```sh
git clone https://github.com/cazevedo/multi_turtlebot3.git
```

```sh
catkin build
```

# Run
Terminal #1
```sh
roslaunch multi_turtlebot3 home_world.launch
```

Terminal #2
```sh
roslaunch multi_turtlebot3 home_world_robots.launch
```

Terminal #3
```sh
roslaunch multi_turtlebot3 turtlebot3_navigation.launch
```
