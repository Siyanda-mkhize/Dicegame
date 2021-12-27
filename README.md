# Dicegame
Artificial Intelligence Coursework 
Introduction 

This assignment requires an agent be written that can play a variant of dice games.

The game has the following rules: 

1) Start with 0 points 
2) Roll three six-sided dice 
3) Choose one of the following: 
	3.1) Stick, accept the values shown. If two or more dice show the same values, then all of them are flipped 	
	     upside down. 1 becomes 6, 2 becomes 5, 3 becomes 4, and vice versa. The total is then added to your points and this is your final score. 
        3.2) Or reroll the dice. Any dice can be held and not rerolled, rerolling incurs a penalty of -1. The max score achievable is 18 however the final score can be 
             negative. 

Two simple agents are provided as examples, which do not perform well. 


Objective 

The objective of the assignment is to write an agent that attempts to maximise the final score by taking any state and returning the following range of actions: stick, hold or reroll. 

Approach 

To achieve the objectives of this assignment a one step look ahead function was implemented as a helper function. The one step look ahead function calculates the action values for each action and stores it in a dictionary and returns the expected value of each action as action_values. 

value iteration is implemented as the main function. The Bellman equation is the basis of the value iteration algorithm and this is evident as the helper function forms an integral part of the value iteration by computing the action values. Once this is done it becomes possible to select the best action to perform based on the highest state-action value. The delta and V are updated and this loop ends once there is convergence. The optimal policy goes through a similar process however it for loops through the game.states and actions. 

The discount rate/gamma is set to one in order to put emphasis on the long-term and maximise rewards. Theta is set to 0.1 in order to increase the average time since lower values only increased the average time. 

Reference 

Choudhary, A. (2018). Nuts & Bolts of Reinforcement Learning: Model Based Planning using Dynamic Programming. Analytics Vidhya. 
 
