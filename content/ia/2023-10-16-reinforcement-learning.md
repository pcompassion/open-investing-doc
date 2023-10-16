+++
title = "Reinforcement learning"
author = ["littlehome"]
date = 2023-10-16
lastmod = 2023-10-16T16:39:56+09:00
draft = false
+++

## Bellman equation {#bellman-equation}

<https://chat.openai.com/share/4def344b-c94f-4194-a428-adbeb4d12175>

It seems one of the backbone idea of reinforcement learning when we want to have a formula to update the decision process.

Bellman specifically provides the goal function that the agent can try to optimize. (it's called value function)

It was used in the Q-learning algorithm for frozen-lake example.
It is used in Monte carlo method for updating the estimates.


## Monte Carlo method {#monte-carlo-method}

<https://chat.openai.com/share/2b0b9c46-4744-4e46-93cb-aca8e02716e0>


### algorithm {#algorithm}

initialize estimator (either Q or V) and policy (P)

For each episode (complete run of a single test)

-   generate episode using the policy
    -   agent in state S takes action and get a reward r
        generate (S: state, a: action, r: reward)
    -   update what you can expect when taking action (S, a)
        update Q(S, a) or V(S)
    -   update policy (in state S, what action you will prefer probablistically)


### On top of goal function (such as bellman equation), it adds another layer of random variables. {#on-top-of-goal-function--such-as-bellman-equation--it-adds-another-layer-of-random-variables-dot}

1.  state, action -&gt; next state mapping is not deterministic, it is probabilistic
2.  reward for taking action can be probablistic
