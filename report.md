# Navigation Project Report

## 1. Goal
The goal of the agent is to collect as many yellow bananas as possible while avoiding blue bananas.  The agent must get an average score of +13 over 100 consecutive episodes.

## 2. Unity Environment

### 2.1 state
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. 
### 2.2 Action
Four discrete actions are available as follow:

0 - move forward.\
1 - move backward.\
2 - turn left.\
3 - turn right.

### 2.3 Reward
Reward is either +1 or -1: +1 for collecting a yellow banana, and -1 for collecting a blue banana. 

## 3. Neural Network Architecture
The NN implemented as fully connected with relu activation function in PyTorch with:
* input layer with 37 nodes, corresponding to the state size
* three hidden layers each with 64 nodes
* output layer with four outputs, corresponding to the four possible actions

## 4. The Agent
The DQN agent approximates the Action-Value function, without a Q-Tables. Q-Tables is utilized in traditional Q-Learning to track states and their expected value of taking an action. The Agent in this project approximates the Q-Table based on the [DeepMind](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf) paper.

The following two techniques were implemented for learning:
* Experience Replay: the experience replay [algorithm](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf) was proposed to uncorrelate the traning samples/ observations, and thus increase the network convergance. In the experience replay, a subset of previous experiences are randomely selected from sample transition pool to make the observations uncorrelated.

* Fixed Q-Targets: when an agent does not have sufficent knowledge to choose the best next action, an additional network, so called Fixed Q-netowrk, can prevent the oscillation of the weights and hence increase convegrance and stability. The weights of the Fixed Q-Target network are updated with the active Q-Target network periodically. The update can be done soft, via a simple weighting function, or hard, Q = Q'. The Fixed Q-Target network is used for evaluation.

At each step, an agent will take an epsilon greedy action, save the experience in the memory. The agent also learns periodically, where the number of steps reaches a specific number.

## 5. Training Parameters and Procedure
