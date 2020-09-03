Learning from Environment
====
Learning from ineteraction is a foundamental idea underlying nearly all theories of learning and intelligence.


## Reinforcement Learning Notes

#### Chapter I Introduction

* Learning from interaction is a foundational idea underlying nearly all theories of learning and intelligence.
* Here we explore a computational approach to learning from interaction.
* RL is much more focused on goal-oriented learning from interaction than are other approaches to machine learning.



##### 1.1 Reinforcement Learning

###### Basic Concepts

* Learning how to **map situations to actions**, so as to maximize a numerical reward signal.
* The learner discovers which action yield the most reward after being training, not which action to take.
* Two features:
  * trail-and-error
  * delayed reward - actions may affect both immediate reward and the **next situation**, all **subsequent rewards**.
* [?]The distinction between problems and solution methods is very important in reinforcement learning.
* Idea of RL is from dynamical system theory, specially, as the **optimal control of incompletely-known Markov decision process**.
* Three aspects that Markov decision process are intended to include:
  * sensation
  * action
  * goal

###### Differences between SL and USL

Supervised Learning

* Each example is a description of a situation together with a specification - the label - of **the** correct action the system should take to that situation. (e.g. categorization)
* The object is for the system to **extrapolate**. (its responses so that it acts correctly in situations not present in the training set)
* But it's impractical to obtain examples represent **all** situations that agent has to act in interactive problems.
* In uncharted territory, an agent must be able to learn from its own experience.



### Vocabulary

trivialize - 琐碎

extrapolate - 外推 - extend the application (based on statistic) to an unknown situation by assuming that existing trends will continue or similar methods will be applicable

impractical - 不切实际的

uncharted territory - 未知领域

intend - 准备
