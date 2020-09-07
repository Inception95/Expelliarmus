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



##### 1.4 Limitations and Scope

RL relies heavily on the concept of state -- as input to the policy and value function, and as both input to and output from the model.

###### State

* Signal conveying to agent some sense of "**how the environment is**" at some time t.
* Formal definition: by the framework of **Markov decision processe**s.
* (?) Concern in this book is not with designing the state signal, but with deciding **what action to take as a function of whatever state signal is available**. (need to write ReByString)

###### Evolutionary Methods (not cover in this book)

* Definition: The policies that obtain the most reward, and random variations of them, are **carried over to the next generation of policies**, and the **process repeats**.
* Advantages: Can be used on problems in which the learning agent **cannot sense the complete state** of its environment.



##### 1.5 An Extended Example: Tic-Tac-Toe

###### Minimax algorithm

First to introduce the based inequality: min-max inequality

(Images/Min-Max%20Inequality.PNG)

* 对于以w为变量情况下的所有下确界中，存在一个以z为变量的上确界A值；对于以z为变量情况下的所有上确界中，存在一个以w为变量的下确界B值；A不大于B。(其中上、下确界指该界的值大于或者小于所有函数值，但是不一定存在函数值等于这个界值，即不一定取到界值的时候函数有定义)

Proof:https://en.wikipedia.org/wiki/Max%E2%80%93min_inequality#:~:text=When%20equality%20holds%20one%20says,equality%20does%20not%20always%20hold.

For the Minimax algorithm, please refer to this blog: https://blog.csdn.net/witnessai1/article/details/78377544



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
