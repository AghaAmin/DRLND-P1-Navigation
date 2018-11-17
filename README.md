# Project 1: Navigation
![alt text](https://github.com/AghaAmin/DRLND-P1-Navigation/blob/master/images/banana.gif)

For this project, we will train an agent to navigate (and collect bananas!) in a large, square world.

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

0 - move forward.\
1 - move backward.\
2 - turn left.\
3 - turn right.

The task is episodic, and in order to solve the environment, an agent must get an average score of +13 over 100 consecutive episodes.


## Getting started
1- Please follow the [udacity instructions here](https://github.com/udacity/deep-reinforcement-learning#dependencies) to set up the environment.

2- Clone this repository onto your local machine

3- Download the banana environment from one of the links below. You need only select the environment that matches your operating system:
* Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
* Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
* Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
* Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

4- Run Navigation.ipynb file in Jupyter Notebook (jupyter notebook Navigation.ipynb). Please make sure the kernel is drlnd.

