# DeepRL-trade
Algorithmic Trading Using Deep Reinforcement Learning algorithms (PPO and DQN)

---

## Introduction:

In quantitative finance, stock trading is essentially a dynamic decision problem, that is, deciding where, at what price, and how much to trade in a highly stochastic, dynamic, and complex stock market. With recent advances in deep reinforcement learning (DRL) methods, sequential dynamic decision problems can be modeled and solved with a human-like approach.

<br>

In this poject, we examine the potential and performance of deep reinforcement learning to optimize stock trading strategies and thus maximize investment returns. Google stock is selected as our trading stock and the daily opening and closing price along with trading volume and several technical indicators are used as a training environment and trading market.

<br>

We present two trading agents based on deep reinforcement learning, one using Proximal Policy Otimization algorithm and the other based on Deep Q-Learing, to autonomously make trading decisions and generate returns in dynamic financial markets. The performance of these intelligent agents is compared with the performance of the buy and hold strategy. And at the end, it is shown that the proposed deep reinforcement learning approach performs better than the buy and hold benchmark in terms of risk assessment criteria and portfolio return.

---

## Project Description:

Two deep RL agents are trained using google stock data **(GOOG)** from **01-01-2014** to **01-08-2022**. **Proximal Policy Optimization (PPO)** and **Deep Q-Learning (DQL)**.

The stable-baselines3 implementations where used for both agents. Both PPO and DQL use Discrete action spaces (1 for complete **Long** position, 0 for complete **Cash** position, and -1 for **Short** position equal to the agent's current asset values).

The trading environments are implemented with the OpenAI gym interface for the agents to interact with. In this environment, agent moves to the beginning of the next trading day by taking an action (1, 0, or -1) at each timestep (day), and recieves a reward equal to the percentage of its total asset value change.

---

## References:
* Human-level control through deep reinforcement learning (Deep Q-Learning) : [paper](https://www.nature.com/articles/nature14236)
* Proximal Policy Optimization) : [paper](https://arxiv.org/abs/1707.06347), [blog](https://openai.com/blog/openai-baselines-ppo/), [spinning-up](https://spinningup.openai.com/en/latest/algorithms/ppo.html)
