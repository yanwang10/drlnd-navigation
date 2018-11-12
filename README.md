# Navigation

This repository is my personal work for the first project of Udacity Deep
Reinforcement Learning Nanodegree. In this project, a special version of Unity
ML enviornment is setup as the task for which we will train an agent to interact
with. Most part of the implementation is from the mini project, Q-Learning. The
model structure is slightly modified to get better performance in this
enviornment.

## The Task

The task is based on the
[Banana Collector](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#banana-collector)
from Unity ml-agent project. The set up is simplifed as one single-agent
(originally it is a multi-agent set up) trying to collect more yellow bananas
(+1 reward for each yellow banana collected) while avoiding blue bananas (-1
reward for each blue banana collected). During exploration of the environment
prepared by Udacity for this project, there are 300 steps for one single
episode, and this task is regarded to be solved when the agent gets >= 13 reward
per episode (the moving average within a window of 30 episodes). In the basic
requirement the agent could see 37 of the internal states, while in the optional
set up the agent could only see visual frames of size 84*84.

Honestly until now I still don't understand what do those 37 dimensions of
observations stand for. I didn't find much document for this project; instead
the original document from Unity ml-agent says there are 53 dimensions of
observation:

```
Vector Observation space: 53 corresponding to velocity of agent (2), whether
agent is frozen and/or shot its laser (2), plus ray-based perception of objects
around agent's forward direction (49; 7 raycast angles with 7 measurements for
each).
```

But this isn't a blocking issue for implementing the algorithm and choose a
model structure and hyper-parameters to train an agent that achieves decent
performance (in terms of episodic rewards).

## Installation

The dependencies of the projects in this Nanodegree are listed in this
[document](https://github.com/udacity/deep-reinforcement-learning#dependencies)
from Udacity. As for this specific project,
[here](https://github.com/udacity/deep-reinforcement-learning/tree/master/p1_navigation)
is the repository containing the instruction of additional set-ups and the
starter code. We don't need to actually install Unity since the enviornment used
in this project is already provided with a pre-built Unity app.

To run the code, please refer to the notebook
[Navigation.ipynb](./Navigation.ipynb).

## Reports

[Report](./Navigation.html) to the benchmark version that takes state
observations as input.

