# Robotics_Deep_RL_Project

##Introduction 

The work presented here trains a robotic arm manipulator using Deep Q-learning Neural Network as the agent. The gazebo simulation environment define the environment as follows: 

• The robotic arm with a gripper attached to it.

• A camera sensor, to capture images to feed into the DQN.

• A cylindrical object or prop. 

The RL task is episodic and the goal is to train the robotic arm manipulator to: 

• At first have any part of the robot arm touch the object of interest 

• Then have only the gripper base of the robot arm touch the object

To launch the project for the first time, run the following in the terminal of the desktop gui:

$ cd /home/workspace/RoboND-DeepRL-Project/build/x86_64/bin

$ ./gazebo-arm.sh

The submission zip file contains entire project folder. The C++ file ArmPlugin.cpp generates the DQN agent responsible for executing the project.
It can be tracked at following path:

RoboND-DeepRL-Project\gazebo\ArmPlugin.cpp

Alternatively, it is kept seperately in this project folder for review.


##Rewards

Following are the list of the rewards used for this project: 
1. Reward based on collision between the arm and the object 

2. Reward based on collision between the arm’s gripper base and the object.

3. Reward for robot gripper hitting the ground 

4. Interim reward based on the distance to the object

##Advantages/Disadvantages 

The RL agent created for this task uses C/C++ API to solve RL problems. It has several advantages: 

• Leverages the power of GPU acceleration to speed up RL agent training 

• Provides popular RL algorithms in library form that can be integrated with robots and simulators 

• Increases execution performance by using C/C++ compilation instead of interpreted python scripts 

One of the drawbacks for this method is that it takes long time to train. A high replay memory quickly destabilize the training process.
