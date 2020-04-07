---
layout: post
title: 'Reinforcement Learning, an introduction'
published: true
---

Let's start with a question. How did you learn to walk? Answer to this question will become more apparent after you think about the following question. How would you train your dog to do some specific tasks? The idea of giving your dog a reward after it performs the given task might not be a bad one. This small idea is what Reinforcement Learning is based upon.

The idea of reinforcement learning is derived from human nature. We love it when our brain produces the dopamine hormone. So, we tend to do tasks that release dopamine hormones. In other words, we inherently want to gain more rewards on a continuous basis. “We” used in this context, in Reinforcement Learning, is referred to as an agent who performs the actions. Everything in reinforcement learning happens in something called the environment. The environment provides the state and based upon the actions performed by the agent, it provides the reward on the basis of policy function. The agent’s goal is to maximize the cumulative reward. In essence, RL is a learning process through interaction with the environment.

![Credit: Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Reinforcement_learning_diagram.svg/250px-Reinforcement_learning_diagram.svg.png)

As shown in the above figure, the agent does the action which is provided to the environment. Then, on the basis of the action provided by the agent and the current state, the environment provides rewards and states. As said before, the agent is trained to choose the action so as to maximize the reward.

This brings us to the MDPs (Markov Decision Process). Before we try to understand MDP, first let’s know about Markov’s property. Any stochastic process is said to have Markov’s property if the probability distribution of the future state depends only on the present state, not on the past states. The following example will make things more clear.

Suppose you have a wardrobe containing a red shirt and two black shirts. Let’s consider the draws are without replacement. Suppose, we made a draw yesterday, and we make a draw today and we will be making another draw tomorrow. If we draw a black shirt today, the probability of drawing a black shirt tomorrow will not only depend on today’s draw but also on yesterday’s draw. If yesterday’s draw gave us a black shirt, we’ll get a red shirt tomorrow. Otherwise, a black shirt. Here, the probability of tomorrow’s event depended not only on today’s outcome but also on yesterday’s outcome. Hence, this stochastic process doesn’t satisfy the Markov’s property.

The use of Markov’s property comes in Markov Decision Process. It can be defined as:

1. a set of States
2. a set of rewards
3. the probability that action A’ in state S’ in timestep t will lead to state S” with some reward in     timestep t+1.

The majority of research in the field of Reinforcement Learning assumes the Markov property. In simpler terms, many RL works assume that the information needed for the future steps are all contained in the present state and so we don’t need to remember anything about the past. This assumption simplifies the task in hand. Hence, Markov’s Decision Process helps to formulate the formal definition of a problem which we are tackling.
