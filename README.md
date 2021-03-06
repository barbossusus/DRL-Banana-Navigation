# UDACITY Deep Reinforcement Learning

[//]: # (Image References)

[image1]: https://github.com/andreifsolomon/DRL-Banana-Navigation/blob/master/duel-dqn-animation.gif?raw=true "Trained Agent"
[image2]: https://github.com/andreifsolomon/DRL-Banana-Navigation/blob/master/notebook_kernel_update.png?raw=true "Kernel"

## Project 1: Unity Banana Navigation

### Introduction

This repository contains an implementation of **Duel Deep Q-Network (DQN)** agent running in a modified [Unity Banana Collector](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#banana-collector) Environment that can be used to train and evaluate models.

### Environment

The agent will navigate in a 3D world created in Unity ML where there are yellow bananas and blue bananas.

### Goal

The goal is to train an agent to navigate (and collect bananas!) in a large, square world.

### Rewards

A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.   

![Trained Agent][image1]

Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.  

### State Space

The state space has 37 dimensions and contains:
* the agent's velocity
* ray-based perception of objects around agent's forward direction.  

Given this information, the agent has to learn how to best select actions.

### Action Space

Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.



### Getting Started

1. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.

2. Place the downloaded zip file in the GitHub repository, in the `DRL-Banana-Navigation/` (current) folder, and unzip (or decompress) the file. 



## Dependencies

To set up your python environment to run the code in this repository, follow the instructions below.

1. Create (and activate) a new environment with Python 3.6 or 3.7.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.7
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.7 
	activate drlnd
	```
	
2. Clone the repository (if you haven't already!), and navigate to the `udacity-ml-agents/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/andreifsolomon/DRL-Banana-Navigation.git
cd deep-reinforcement-learning/udacity-ml-agents
pip install .
```

3. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.  
```bash
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```

4. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

![Kernel][image2]


### Repository Contents

- **Navigation.ipynb** - this is a notebook that contains the training code
- **Navigation-Viewer.ipynb** - notebook that can be used to view the final model, saved as 'model.pth'
- **dqn_agent.py** - this contains the implementation of the agent and the replay buffer
- **model.py** - contains the QNetwork and DuelQNetwork implementations. The second one is used in this project/demo.

- **model.pth** - final saved weights after training


### Instructions

Follow the instructions in `Navigation.ipynb` to get started with training the agent!  
When done execute `Navigation-Viewer.ipynb` to view the trained model results.

