# banana_navigation
Udacity Deep RL Banana navigation project

Project Details

The project is to train an agent to collect yellow bananas for reeward of +1 (and avoid blue bananas for reward of -1) in the Banana Unity Environment, by using Deep Reinforcement Learning through DQN and it's variants. The environment has 37 state dimensions with 4 possible actions (front, back, left, right). The environment is considered solved when the model achieves a score of 13 or more.


Getting Started

The dependencies for the progream are in requirements.txt file, following the instrcutions in https://github.com/udacity/Value-based-methods#dependencies, with the banana unity environment sourced directly from (for Linux) https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip and extracted and placed in the p1_navigation/ folder. After that cuda support was installed using conda install cudatoolkit

Instructions

The entire code is in Navigation.ipynb. To execute, run upto cell "In [2]" (under 2. Examine the State and Action Spaces) sequentially, to load and examine the environment. You can explore the environment to see random actions being taken by executing the next cell. Then execute cells "In [13]" for class definition (QNetowrk, DQN Agent, ReplayBuffer classes), and "In [14]" to build the agent. You can set the following for trying variants of the regular DQN (The setting below is for Dueling DDQN, which gives the best results).

DOUBLE_DQN = True
PRIORITIZED_EXPERIENCE_REPLAY = False
DUELING_DQN = True

Then there are two options
(1) To train - Execute the next cell "In [15]", which will train and output the status of training, ending with a plot of the score. This will save the best model in the 'checkpoint.pth' file
(2) Alternatively, execute the model without training by loading the pretrained weights from the 'checkpoint.pth' file, by running the cell "In [16]" 

Lastly, run the env.close() cell, when finished.

