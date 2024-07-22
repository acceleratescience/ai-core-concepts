# Reinforcement Learning


## Learning Objectives

This section will help you understand:

- What reinforcement learning is
- Some real-world examples of reinforcement learning in research



## What is Reinforcement Learning?
Reinforcement learning is a type of machine learning aimed at tasks where the machine, or _agent_, has to take a series of moves in an uncertain and changing environment, to achieve a specific goal. The agent learns a strategy, or _policy_, that guides how to take actions based on the current state of the agent within the environment.

A typical application of reinforcement learning is in playing games. Some of the biggest breakthroughs in the field have come through playing board games like Go, or video games like StarCraft. Reinforcement learning models optimise a _reward_. In gaming that reward would be high if they win the game, and low if they lose. In gaming, the environment is uncertain because there are multiple players, and it’s not possible to know what moves each player will make. It’s also not possible to know the winner of the game, and hence the final reward, until the game has completed. Thus, the correct choice of action by the agent at any time must take into account indirect and delayed consequences of that action in the future, and hence requires a form of _planning_.

Another example of reinforcement learning is for controlling robots in a lab environment. Here, the sensors on the robot have some uncertainty in their measurements, and the lab environment may change based on what people in the lab are doing. The reward for the robot is high if they successfully complete their task, and low if they fail.

Unlike supervised and unsupervised learning, which learn their behaviour from fixed datasets, reinforcement learning agents learn through repeated interactions with the environment. Agents begin with random behaviour, and through training in a trial-and-error fashion they learn to exhibit the desired behaviour. Often it is too time-consuming and expensive to learn entirely through direct interaction, and so a simulated environment is often used in training. This is why video games are a great testbed, as they are inherently a simulation.

During learning, reinforcement learning algorithms rely on a mixture of _exploration_, or trying new actions to discover what works, and _exploitation_, which is trying actions that have already been proven to work in order to maximise the reward.

 In practice, reinforcement learning is used much less than supervised and unsupervised learning as it is more complicated to implement and to achieve good results.



## Reinforcement Learning Use Cases
RL is used in scenarios like:

- Playing games, where the computer can choose to make optimal moves but there is some uncertainty about the moves its opponent may make.
- Controlling robots in real-world environments such as the lab, where there is uncertainty about how the environment changes over time.
- Identification of novel drug candidates. In this task, actions available to the agent are modifications to molecules, and the reward function provides feedback about desired properties of the molecules. 
- In quantum Physics, reinforcement learning has been applied to the problem of finding sequences of commands for manipulating the states of a quantum system in a controlled manner. 


In each of these tasks, it’s hard to judge in isolation whether a single turn or move by the computer is optimal. Yet, we do know in the long-term whether the computer achieves its goal.


## Inspiration

- [One famous example of reinforcement learning is Deepmind's AlphaGo model, that learned to play the game Go](https://deepmind.google/technologies/alphago/)


## Contact

If you can't find what you need

[CONTACT US :fontawesome-solid-paper-plane:](mailto:accelerate-mle@cst.cam.ac.uk){ .md-button }





