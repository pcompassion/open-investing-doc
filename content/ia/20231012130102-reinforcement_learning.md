+++
title = "reinforcement learning"
author = ["littlehome"]
lastmod = 2023-10-12T18:18:42+09:00
draft = false
+++

## chatgpt conversation {#chatgpt-conversation}

[chatgpt conversation]({{< relref "rl.md" >}})


### Frozen Lake (Q-learning) {#frozen-lake--q-learning}

[frozen lake (Q learning) implementation]({{< relref "20231012163349-frozen_lake.md" >}})


### Frozen Lake (policy gradient) {#frozen-lake--policy-gradient}

[implementation]({{< relref "20231012163349-frozen_lake.md" >}})


### heuristic aspect of RI {#heuristic-aspect-of-ri}


## definition {#definition}

There is a goal.
Goal can be measured numerically in intermediate states. (Reward)

Find a way to reach the goal using the reward as hint.
One often has to react to intermediate state (without perfect information)
Often, model it by using decision (Policy) acting on the perceived state


## property {#property}

The environment is not perfectly modeled (understood)
Yet we try to come up with model which will react to environment so that we can reach the goal

Guiding data is different from supervised learning

-   no annotated data
-   guiding data creation is part of learning process
    -   which can be random


## next learning objective {#next-learning-objective}

<https://developer.ibm.com/learningpaths/get-started-automated-ai-for-decision-making-api/what-is-automated-ai-for-decision-making/>
