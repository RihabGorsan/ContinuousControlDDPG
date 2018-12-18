# Continuous Control project: p2 in DRLND 
---
## Project details: 

This is the second project in the Udacity Deep Reinforcement Learning Nanodegree, a four month course that I am taking. The environment for this project involves controlling a double-jointed arm, to reach target locations.
<p align="center"><img src="unity_reacher.gif" width="50%" style="middle"></p>


## Environment details: 

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.
</br>
The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.
The task is episodic.
</br>

In this repo, we will play around the second version of the reacher environment that contains 20 agents.</br>
The environment is considered solved when the agent get an average score of +30 over 100 consecutive episodes.
## Getting started

1. Clone this repo using `git clone https://github.com/RihabGorsan/ContinuousControlDDPG.git` </br>
2. Begin by importing the necessary packages. So first create a conda environment  </br>
`conda create --name navigation python=3.6` </br>
and then install the following packages: </br>
`conda install -y pytorch -c pytorch` </br>
`pip install unityagents==0.4.0 ` </br>
`pip install mlagents` </br>

3. Download the Banana unity environment 
You can download the environment form one  of the links below. Just please select the enviornment that matches your OS </br>
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip) </br>
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip) </br>
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip) </br>
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip) </br>

Unzip the file hen place it in the cloned project. 

## Train your agent
You can execute each code block in the ddpg notebook to train the agent using DDPG.  This will fire up the Unity environment and output live training statistics to the command line.  When training is finished you'll have the two saved models in `checkpoint_actor.pth` and  `checkpoint_critic.pth`.

And following are the results of the training:
```
Episode 1	Average Score: 0.13
Episode 2	Average Score: 0.24
Episode 3	Average Score: 0.28
...
Episode 241	Average Score: 29.72
Episode 242	Average Score: 30.00
Episode 243	Average Score: 30.27
Enviroment solved in @ i_episode=243, w/ avg_score=30.27
```

Feel free to experiment with modifying the hyperparameters to see how it affects training:

- [model.py](model.py) : you can change the architecture of the network.
- [ddpy_agent.py](ddpg_agent.py) : play with the hyperparams of the RL agent.

## Report
See the [report](report.md) for more details.  


