# TicTacToe_QLearning
Deep Q Learning algorithm implementation for Tic Tac Toe. <br/>

# Description
This notebook contains code for Q Learning along with environment for playing the game.<br/>
The code is written in non oop manner for easier manipulation of constraints during training.<br/>

Custom environment for TIC TAC TOE is written from scratch.<br/>
The jupyter notebook has different cells for initialization, training and for playing with agent or 2 agents playing against each other.<br/>
Each cell has comments regarding what it does and cells are in order of execution.<br/>

# Controls
The numpad is mapped as 3x3 grid. <br/>
Player can use numpad as grid to play with agent.<br/>
For example 7 on numpad referes to top left box in the board.<br/>

# Training
4 Neural Networks are initialized, 2 for each agent.
Each agent has a training network and a target network. <br/>
Q values for all possible states of game are given by the agent's network and according to the Q values, the next action is determined.<br/>
To train the models, experience tuples are collected which contain:<br/>
Current State (S), Action Taken (A), Reward (R), Next State(S'), Game State (A).

The Game State stores data about completion of game.<br/>

![Deep Q Learning Algorithm](https://www.researchgate.net/publication/345893622/figure/fig2/AS:1083898943545355@1635433054806/Flow-chart-of-the-deep-Q-learning-network.jpg)<br/>

The training is divided into 20 iterations of 20,000 games. <br/>
All interations have varied values of epsilon, decay and firstRandom variables. <br/>
firstRandom is a Boolean variable that decides if first move of the agents will be random or not. <br/>
It is implemented in order to increase exploration in some training stages. <br/>
During training these 3 variables are varied to improve results. <br/>
The target network is updated after few iterations same as evaluation/training network. <br/>

After the training it has learned to play fairly well against player.<br/>
But I think with more tuning of variables and more iterations, there is still room for improvement. <br/>

# Gameplay


# Files
I have included all 4 networks which I found to be best performing. <br/>
To load those networks, run the "Model Load" labelled cell.<br/>

