**Clone my exploration package repository into src**
`git clone https://github.com/your_github_username/m-explore-ros2.git`

**Install dependencies**
`sudo apt update`
`sudo apt install ros-humble-turtlebot3* ros-humble-navigation2 ros-humble-nav2-bringup`

**Build your workspace**
`cd ~/ros2_ws`
`colcon build --symlink-install`
`source install/setup.bash`

**Launch Navigation2 stack and Gazebo simulation server**
`ros2 launch turtlebot3_navigation2 navigation2.launch.py use_sim_time:=True`

**Open Gazebo client (in a new terminal)**
`gzclient`

**Run the frontier exploration node**
`ros2 run frontier_exploration explorer`



**Returning to initial pose**
The robot will return to its initial pose after exploration if you want by defining the parameter return_to_init to True when launching the node.
