# MARL report



## Introduction

This repository is the solution for the third and final assignment in the Udacity Deep Reinforcement Learning Nanodegree. The goal was to train an agent using a Multi Agent DDPG that was able to sucessfully solve the "Tennis" environment made by Unity ML Agent and collect enough rewards, represented by playing a game, in order to achieve a score above a certain threshold. We'll be introducing the Project details.

## Project details

The following iterals contains the description of the environment

a. State

In this case, the state consists of two agents, which are playing on opposite sides of the court facing a net and with a ball. Each agent has 8 variables in the observation space, which describe things associated with the position and the velocity of the ball and the racket.

b. Action spaces

Two continuous actions are available for each agent, consisting of moving away or toward the net, and of jumping, respectively. 

It is important to note that the agent doesn't act directly with the environment. A so called "brain" controls the actions within the environment and collects the information from the state.

c. Solved 

The task is episodic (it is not eternal, it ends after a while), and the environment is considered solved when the agents achieve an average score of +0.5 over a window of 100 consecutive episodes (after taking te maximum score of each agent for each episode). 


## Getting started

a. Unity ML Agents:

First you must install the Unity toolkit. You'll find the instruction in this link, please don't dispair, this is probably the hardest step: <href>https://github.com/udacity/deep-reinforcement-learning#dependencies
	
b. Install
	
After you have downloaded the toolkit please install it and then download the tennis environment you can find it in the following link: <href>https://github.com/udacity/deep-reinforcement-learning/tree/master/p3_collab-compet.
	
c. Play
This implementation has 9 files:

* Model.py
-This file contains the implementation of both the actor and the critic class, which the other model uses to run the network. Both of them describe the DNN (Deep Neural Network) used by both the actor and the critic process
* Tennis.ipynb
-Main file that executes the runner.
* Buffer.py
-This file contains the specifications for the replay Buffer
* DDPG_Agent.py
-This file specifies the DDPG agent, and all the steps (learning, acting, etc.) that it has to perform
* OUNoise.py
-File specifying the noise process
* Multiagent_class.py
-This file is a special file that configures the process of having multiple agents act, reset and so forth. It's special because we had to learn how to configure multiple learners.
* Configuration.py
- Finally, this file is the file that sets the hyperparameters to be used in our network (tau, Learning rate, Neural network size, discount factor, etc.)

We want to thank the github community, since if we're honest we didn't have a lot of time for this one, and we had NO idea how to set the Multiagent configuration (hence why that file is special to us).

## Instructions

Just as highlighted above if you want to train the model from scratch run the Tennis jupyter notebook. Otherwise you can use the pretrained checkpoint (denoted as ..._final for both actor and critic) provided in the repository. 
