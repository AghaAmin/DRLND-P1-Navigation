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

