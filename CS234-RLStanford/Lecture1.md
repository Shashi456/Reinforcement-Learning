# Lecture 1 - Introduction
## Key points
- Reinforcement learning is concerned fundamentally with, "How does an intelligent agent learn to make good sequences of decision?"
- Deepmind Nature, 2015 paper on Atari.
- Video games are good enough examples of complex tasks that takes humans time to learn. For an agent this is just seen as pixels and its interesting to see how it learns how to play it.
- Educational Games - Madel et al 2014 AAMAS.
- RL is also used in NLP and CV.
- Reinforcment learning involves optimization, delayed consequences, exploration and generalization.
- Delayed consequences involves asking questions like, "how do you decide long term consequences of a decision"
- Policy is mapping from past experience to action.
- AI planning involves everything similar to RL except exploration.
- Supervised ML involves optimization and generalization, it also involves learning from experiences and has labels from world.
- Unsupervised ML involves optimization and generalization, it also involves learning from experiences and has no labels from the world.
- Imitation learning is similar to RL, it involes optimization, generalization, delayed consequences, learns from experiences of others, Assumes input demos of good policies. Eg: Abbeel, Coates and Ng helicopter examples. Imitation learning reduces RL to supervised learning, which is useful but collecting such data is hard.
- There are a variety of challenges in learning to make sequences of good decisions. Planning being one of them.
## Sequential Decisions made under uncertainty
<img src= "./images/cs234/lecture1/Agent.png">
- Agent takes some action in the world and there is some observation/reward feeded back to the agent.
- The goal is to maximize expected reward, expected because we might be dealing with stochastic processes.
- Example - Ad recommendation, blood pressure control, Robotic arm control.
- Machine Teaching.
- History is the sequence of past observations, actions & rewards.
- State space is the representation of the world.
- World state is the real world.
- Markov assumption: future is independent of the past given the present.
- Markov assumption for prior examples.
- (Q:why markov is important?)If you include all the history, then most decisions can be made markov.
- Fully observable : MDP (Markov Decision Process)
- Partially observable : POMDP, Eg: Poker player, healthcare.
### Types of Sequential Decision processes
- Bandits: Actionshave no influences on next observations.
- MDPs and POMDPs: Action influence future observations.
- How the world changes: Deterministic or Stochastic.
## RL algorithm components
-  Model: Agent's representation of how the world changes. Can keep two models Transition model which keeps track of representation, reward model keeeps track of immediate reward.
- Policy: Determines how the agent chooses actions. There can be either a determistic or stochastic policy.
- Value function: expected discounted sum of future rewards under a particular policy. Influenced by discount factor.
## Types of RL models
- Model based : Explicit representation of a model, may or may not have a policy or value function.
- Model Free : Explicit representation of policy or value, no model.
<img src= "./images/cs234/lecture1/rltypes.png">
## Exploration and Exploitation
- Should the agent explore various actions or should it exploit what it already knows?
- (Doubt: Can we have an exploration model, i.e give suggestions of what it should explore?)
- Finite and infinite horizon problems.
## Evaluation and control
- Evaluation of a given policy i.e estimate/predict the expected rewards.
- Control : Optimization i.e find the best policy.
