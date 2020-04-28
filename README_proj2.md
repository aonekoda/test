[//]: # (Image References)
[image1]:https://video.udacity-data.com/topher/2018/June/5b1ea778_reacher/reacher.gif "reacher"


# Project 2 : Continuous Control

---

## Introduction
For this project, you will work with the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

![reacher][image1]

#### Summary of Environment
* Set-up: Double-jointed arm which can move to target locations.
* Goal: Each agent must move its hand to the goal location, and keep it there.
* Agents: The environment contains 20 agents linked to a single Brain.
* Agent Reward Function (independent):
    * +0.1 for each timestep agent's hand is in goal location.
* Brains: One Brain with the following observation/action space.
    * Vector Observation space: 33 variables corresponding to position, rotation, velocity, and angular velocities of the two arm Rigidbodies.
    * Vector Action space: (Continuous) Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.
    * Visual Observations: None.
* Reset Parameters: Two, corresponding to goal size, and goal movement speed.
* Benchmark Mean Reward: 30


#### Goal
The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.


## Getting Started

1. Download the Unity environment with the Agents  

    Download the environment from one of the links below and decompress the file into your project folder. You need only select the environment that matches your operating system:

 * Version 1: One (1) Agent
     * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
     * Linux Headless: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip)
     * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
     * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
     * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)
 * Version 2: Twenty (20) Agents
     * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
     * Linux Headless: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip)
     * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
     * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
     * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)     

    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining whether your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) (version 1) or [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) (version 2) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)


2. Place the file in the [DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning), in the `p2_continuous-control/` folder, and unzip (or decompress) the file.

3. Dependancies  
    - Please reference `require.txt` [this link](https://github.com/udacity/deep-reinforcement-learning/blob/master/python/requirements.txt)
    - This is an amended version of the `python/` folder from the [ML-Agents repository](https://github.com/Unity-Technologies/ml-agents).  It has been edited to include a few additional pip packages needed for the Deep Reinforcement Learning Nanodegree program.

## Instructions

The notebook `Continuous_Control.ipynb` contains the code to set up the environment and the outer episode iteration to solve the reinforcement problem. 

## References
* Deep Deterministic Policy Gradients (DDPG) ([this link](https://arxiv.org/abs/1509.02971))
* Udacity single-agent DDPG ([this link](https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum))
