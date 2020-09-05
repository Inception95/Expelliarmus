Learning from Environment
====
Learning from ineteraction is a foundamental idea underlying nearly all theories of learning and intelligence.


## Reinforcement Learning Notes

#### Chapter I Introduction

* Learning from interaction is a foundational idea underlying nearly all theories of learning and intelligence.
* Here we explore a computational approach to learning from interaction.
* RL is much more focused on goal-oriented learning from interaction than are other approaches to machine learning.



##### 1.1 Reinforcement Learning

##### Basic Concepts

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



##### Differences between SL and USL

###### Supervised Learning

* Each example is a description of a situation together with a specification - the label - of **the** correct action the system should take to that situation. (e.g. categorization)
* The object is for the system to **extrapolate**. (its responses so that it acts correctly in situations not present in the training set)
* But it's impractical to obtain examples represent **all** situations that agent has to act in interactive problems.
* In uncharted territory, an agent must be able to learn from its own experience.

###### Unsupervised Learning

* Finding structure hidden in collections of unlabeled data.
* Maximizing a reward signal (RL) is different from trying to find the hidden structure (USL).



##### Challenges when we talk about RL

###### Two key challenges

* Trade-off between **exploration** and exploitation
  * Agent has to **exploit** what it has already **experienced** to obtain reward.
  * Agent also has to **explore** to make better action (may **not be taken before**) selections in the future.
* RL explicitly considers the whole problem of a **goal-directed** agent interacting with an **uncertain environment**
  * Other approaches might failed to consider the subproblems by addressing how they might fit into a larger picture.
  * That is, in the contrary, RL starts with a **complete, interactive, goal-seeking** agent.
  * The agent **has to operate** despite significant uncertainty about the environment it faces.
  * *SL in RL is to determine which capabilities are critical and which are not.



##### Example of a complete, interactive, goal-seeking agent

It does not always mean a complete organism or robot.

E.g. An agent that monitors the charge level of robot's battery and send commands to the robot's control architecture. 

* Environment: the rest of the robot **together with** the robot's environment
* This time the agent is a **component** of a larger behaving system.



##### Other interesting findings

* Modern RL has substantive and fruitful interactions with other **engineering and scientific disciplines**.
* Some RL methods can learn with parameterized approximators addresses the classical "**curse of dimensionality**" in operation research and control theory.
* Many of core algorithms of RL were originally inspired by biological learning systems.
* Methods
  * "weak methods" - those based on general principles, such as **search or learning**.
  * "strong methods" - those based on **specific knowledge**.



##### 1.3 Elements of Reinforcement Learning

###### Four main subelements of a reinforcement learning system

* Policy
  * defines the agent's way of behaving at a given time.
  * mapping from **perceived states** of the environment to **actions to be taken** when in those states.
  * can from **a simple function** or look up table to **stochastic, specifying probabilities** for each action.
* Reward signal
  * defines the **goal** of a RL problem.
  * agent's sole objective is to maximize the total **reward** it receives **over the long run.**
  * e.g. biological system's experiences of **pleasure or pain**.
  * they may be stochastic functions of the state of the environment and the actions taken.
* Value function
  * the value of a state is the total amount of reward an agent can expect to accumulate over the future, starting from that state.
  * reward is **immediate**, intrinsic desirability of states, while values indicate the **long-term** desirability of states after taking into account the states.
  * **WITHOUT rewards there could be no values, and the only purpose of estimating values is to achieve more reward**.
  * much harder to determine values than rewards, rewards are given directly by the environment, but values must be **estimated and re-estimated** from the sequences of observations an agent makes over its **entire lifetime**.
* (Optional) Model of the environment
  * it allows inferences to be made about how the environment will behave.
  * Methods
    * Model-based methods: use models and planning
    * Model-free methods: explicitly trial-and-error learners



### Vocabulary

trivialize - 琐碎

extrapolate - 外推 - extend the application (based on statistic) to an unknown situation by assuming that existing trends will continue or similar methods will be applicable

impractical - 不切实际的

uncharted territory - 未知领域

intend - 准备

exhaustively - 详尽的 - in a way that includes or considers all elements or aspects (=comprehensively)

alongside - 并肩

petroleum refinery - 石油精炼厂

gazelle - 瞪羚

indirect - 间接的

foresight - 远见，深谋远虑
