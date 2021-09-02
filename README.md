# SoFar
Sofar navigation project for UNIGE
Software Architecture Project
Group:NAV_04
Student(s): Nagalakunta Sumanth(5065491), Alluri Sai krishna rama chander raju(5060551), Julio Sebastian Sullca Trillo(5129500),Paraman Hanish Muthurathinam(5060913)
Tutor(s): Fulvio Mastrogiovanni , mohamad Alameh, Alessandro Carfi, Simone Macciò
Gamping:the gamping package provides laser-based SLAM as a ROS node called slam_gamping. By using this we can create 2-D occupancy grid map and pose data collected by a mobile robot.

Rviz: Rviz is a 3d visualization tool for ROS, It provides a view of your robot model,captures sensor information from robot sensors, and replay captured data. It can display datafrom cameras, lasers, from 3D and 2D devices including pictures and point clouds.The robot state publisher helps you to broadcast the state of your robot to the tf transform library. The robot state publisher internally has a kinematic model of the robot, joint positions of the robot, compute and broadcast the 3D pose of each link in the robot.

Move_base: The move_base node provides a ROS interface for configuring, running, and interacting with the navigation stack on a robot. In the absence of dynamic obstacles, the node will eventually get within this tolerance of its goal or signal failure to the user.

Planner: This shows the local costmap that the navigation stack uses for navigation.e. For the robot to avoid collision, the robot's footprint should never intersect with a cell that contains an obstacle.

Navigation: It takes in information from odometry and sensor streams and outputs velocity commands to send to a mobile base.The stack the robot should have a tf transform tree in place, and publish sensor data using the correct ROS Message types. It needs to be configured for the shape and dynamics of a robot to perform at a high level.

Config-file: Contains all robot configuration and definition files, model.rviz: a pre-configured Rviz file including all the necessary data for the Rviz. params.yaml: including Ros-Ip and Unity-Ip for the communication purposes

Launch:Start the simulation on ROS side executing in the workspace:


For localizing the robot in the environment we use:

roslaunch mobile_robot_navigation_project slamgmapping.launch

For launching the simulation of husky:

roslaunch mobile_robot_navigation_project rvizcontroller.launch

For starting comuniation between ROS and UNTY:

roslaunch mobile_robot_navigation_project navigation.launch

For navigation and moving the robot and path planning:

roslaunch mobile_robot_navigation_project movebase.launch
