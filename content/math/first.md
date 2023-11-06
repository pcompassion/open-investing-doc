+++
title = "Statistics"
author = ["littlehome"]
date = 2023-11-06
lastmod = 2023-11-06T14:09:37+09:00
draft = false
+++

math


## introduction to data science {#introduction-to-data-science}

This is my note on taking course on <https://learning.edx.org/course/course-v1:HarvardX+PH125.4x+1T2023/home>

Mostly basic statistics.


## gpt chat {#gpt-chat}

-   overall: <https://chat.openai.com/share/ffce1eb3-c872-48f4-b3fa-22b7bf6d2113>
-   on T distribution: <https://chat.openai.com/share/c123934f-8c91-4c11-9b02-a13ec528db03>
-   on linearity: <https://chat.openai.com/share/71ab41c6-5c63-43ad-9676-8d4ab108f926>


## polling vs forecasting {#polling-vs-forecasting}

polling is looking at current situation, but forecasting uses the data to predict future


## urn model {#urn-model}

With probability assumption or modeling , a bean has probability p.
We can model sum of n beans.
So our sample, sum of n beans, would have properties we know (because of the assumption)
That's how we guess and measure our knolwedge about unknown p


## what's the justification for using our estimate when calculating SE {#what-s-the-justification-for-using-our-estimate-when-calculating-se}

\\[ Pr(|X-p| < 0.1) \\]
why clt works with \\(SE(\bar(X))\\) by plugging in \hat(X) for p
or is it just the best we can do?


### law of large number {#law-of-large-number}

This principle gives us the foundation for using the sample proportion \\( \hat{p} \\) as an estimator for the true population proportion \\( p \\). It tells us that as our sample size increases, \\( \hat{p} \\) will tend to converge to \\( p \\). Thus, the larger our sample, the closer \\( \hat{p} \\) is expected to be to \\( p \\), giving us a solid base to use \\( \hat{p} \\) in place of \\( p \\) when we calculate things like standard error.


### interpretation {#interpretation}

So when we calculate the probability by using our \hat{SE} , it's not mathematically air-tight probability. it can have some error due to our estimate not being equal to parameter, but we still  use the term 'probability' as if it is true probability..
it is , actually, the best probability estimate we can have with data.


## variance {#variance}


### how variable is your success if you have success rate p? {#how-variable-is-your-success-if-you-have-success-rate-p}


### interpretation {#interpretation}

1.  uncertainty (p = 0.5 is high uncertainty) is high variance
    in extreme, p = 1 has no variance

2.  student with high grade will have small variance. (Urn model)

    student with high grade can be thought of having high probability p of getting an answer right.
    and grade is average of those binary event.

3.  batting avg 0.45 after 20 bats is not gonna last (Bayesian Hierarchical model)

    So here, we are saying the opposite, it's not gonna last, and we will see bigger correction for this player.

    In this case, we are not buying that the player indeed has the true probability of 0.45. It is not our best guess for the player.
    So we are using a different assumption when we see a student with high grade.

    This can be expressed quantitatively:

    \\[ \mathbb{E}(p | Y = y) = B\mu + (1 - B)y \\]

    which says, we suspect our observation (the high 0.45) if we think the variation of our observation is large.

    The derivation is at below

4.  so which interpretation is right, why baseball player is different from student?

    Sometimes I associate extreme object might with a big risk: entertainers (with high income) is associated with big sudden downfall.
    If we assume their variance is low, the association is actually false, and suggest that the non variability of the group of high income group makes me to falsely associate small number of instances of divergion from mean as big event (because it is rare among the group)

    Here should I be using urn model or hierarchical model?

    Or am I just being jealous for them to fall from the tree?


## confidence interval {#confidence-interval}


### why call it confidence, not probability {#why-call-it-confidence-not-probability}

It is due to the fact that \\( \hat{SE} \\) is not a probability and it is not same as true \\( \text{SE} \\).

If we take our sampling as one instance of many such sampling, our clt says, we getting this specific sample is related to real probability of this magnitude, but
here we are again using our estimate \\( \hat{SE} \\), so the magnitude itself might be off,
so this is also another .. trick.. or non mathematically air tight probability we are talking about,
we can say something about our estimate with some magnitude, but this magnitude is itself a proxy for a real magnitude we are trying to express.

so when we say interval says how likely (95%) this interval would contain true population is.. not .. again air tight probability statement. (after all it doesn't make sense for two different sample have two different confidence interval with same 95% exact probability)  it's the best we can do to express our  limitation of our modeling (inference)


### simulation {#simulation}

```python

import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import norm
import pandas as pd

d = 0.039
Ns = [1298, 533, 1342, 897, 774, 254, 812, 324, 1291, 1056, 2172, 516]

p = (d+1) / 2

q = 0.95
z = norm.ppf((1+q)/2)
population = np.array([0, 1])  # 0 could represent 'no' and 1 'yes'

b = len(Ns)

x_hat_array = np.array(
    [np.mean(np.random.choice(population, size=size, p=[1-p, p])) for size in Ns])
x_std_hat_array = np.sqrt(x_hat_array * (1-x_hat_array)/ Ns)

intervals = np.array([np.array([x_hat - z * x_std, x_hat + z * x_std]) for x_hat, x_std in zip(x_hat_array, x_std_hat_array) ])
contains_p = [interval[0] < p < interval[1] for interval in intervals ]


plt.subplot(2,1,1)
# Plotting
for i in range(b):
    if contains_p[i]:
        color = 'green'
    else:
        color = 'red'
    plt.plot(intervals[i] *2 -1 , [i, i], color=color, zorder=1)  # Interval line

# Marking the true proportion d
plt.axvline(x=d, color='blue', linestyle='--', label=f'True d={d}')


# aggregate

n = sum(Ns)
p_ns = np.sum(x_hat_array * Ns / sum(Ns))
std_ns = np.sqrt(p_ns * (1-p_ns)/ sum(Ns))

plt.plot(np.array([p_ns - z * std_ns, p_ns + z * std_ns]) * 2 - 1, [b, b], color='blue')

plt.xlabel('Interval')
plt.ylabel('Sample Number')
plt.legend()
plt.grid(True)


plt.subplot(2,1,2)
# Plotting
for i in range(b):
    if contains_p[i]:
        color = 'green'
    else:
        color = 'red'
    plt.plot(intervals[i]  , [i, i], color=color, zorder=1)  # Interval line

# Marking the true proportion d
plt.axvline(x=p, color='blue', linestyle='--', label=f'True p={p}')


# aggregate

n = sum(Ns)
p_ns = np.sum(x_hat_array * Ns / sum(Ns))
std_ns = np.sqrt(p_ns * (1-p_ns)/ sum(Ns))

plt.plot(np.array([p_ns - z * std_ns, p_ns + z * std_ns]), [b, b], color='blue')

plt.xlabel('Interval')
plt.ylabel('Sample Number')
plt.legend()
plt.grid(True)

plt.show()

# a = np.array([p_ns - z * std_ns, p_ns + z * std_ns])
# print(a[1]- a[0])

# a = np.array([p_ns - z * std_ns, p_ns + z * std_ns]) * 2 - 1
# print(a[1]- a[0])
```


### interpretation {#interpretation}

When we deal with \\( d = 2 p - 1\\) (the difference of two candidates), we are exaggerating the estimator by a factor of 2.

So our uncertainty will also be scaled up by the same factor.

\\[ \text{Pr}(X < a) = \text{Pr}(2X - 1 < 2a - 1) \\]

This applies to any distribution.

Our confidence interval bound gets larger and our MoE gets larger by the same factor.


### Nate silver {#nate-silver}

He used the aggregation of many pollsters to predict trump win (so it's not that long ago) for the first time (publicly).
The math behind is simple: large sample size \\( N\\) can reduce the sample variance and thus reduce the confidence interval.
It shows how little we actually understand the math we learn.


## Bayes {#bayes}

So Urn model allowed us to express our uncertainty with confidence interval.
To arrive at confidence interval, we acknowledged what we don't know \\( \hat{p} \\) but used it regardless and we obtained the tool confidence interval.

Can we do more? can we know more by saying we don't know?


### shift of perspective {#shift-of-perspective}

What does it mean when an election forecaster say that a given candidate has a 90% chance of winning?

It would mean \\( \text{Pr}(p>0.5) = 0.9 \\).
Note, when we say a coin has probability, we were saying it has the fixed property called probability associated with the dice. Likewise, we were assuming a candidate has a probability of winning, a fixed probability.

It would not make sense to say a probability of a coin's \\( p \\). Because it was assumed to be a fixed but possibly unknown value.

Bayes, shift that perspective. It says, we don't know the true probability, but we can measure the probability of it having a certain probability of \\( p \\).

It is a very fundamental shift. That we were measuring something objective, and now we say there might not be such objective thing we can talk about, we don't know for sure, but we can quantify our belief on that thing.


### a layer of abstraction {#a-layer-of-abstraction}

So we begin by letting go of our frequentistic notion of probability. The prior probability has that notion.
But then, by updating process, we are again heading back to the true probability.
I.e. the bayesian updating can be thought of as iterative process of going toward the true posterior priority (or true priority in short)


### the counter intuitive {#the-counter-intuitive}

When a test have 99% precision for a rare hidden property, if I succeed on the test, do I have the property?

E.g. When a drug test is 99% accurate, and the test shows I have a disease, do I have the disease?

-   Probability of you having a disease when the test says so: \\( P(\text{Positive}|\text{Disease}) = 0.99 \\)
-   Probability of you not having a disease when the test says so: \\( P(\text{Negative}|\text{No Disease}) = 0.99 \\)

This problem consistently catches me off-guard.
The interpretation is, my brain / thinking is so wired to do the conditional probability. I.e. we take a current situation as the whole world and interpret proabability. We are quick to confine our world into this conditioned world.

```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Probabilities
p_disease = 0.00025
p_no_disease = 1 - p_disease
p_test_positive_given_disease = 0.99
p_test_negative_given_no_disease = 0.99

# Joint probabilities

false_negative = (1 - p_test_positive_given_disease) * p_disease
true_negative = p_test_negative_given_no_disease * p_no_disease

true_positive = p_test_positive_given_disease * p_disease
false_positive = (1 - p_test_negative_given_no_disease) * p_no_disease

N = 100000
# Create a 2x2 array with the probabilities
data = np.array([[false_negative, true_positive],
                 [true_negative, false_positive]]) * N

 # Column and row labels
rows = ('Disease', 'Healthy')
columns = ['- test', '+ test']

# Create a figure and a subplot
fig, ax = plt.subplots()
ax.axis('tight')
ax.axis('off')

# Create the table
table = ax.table(cellText=data,
                 rowLabels=rows,
                 colLabels=columns,
                 cellLoc = 'center',
                 loc='center')

# Scale the table
table.scale(1, 2)

plt.show()

```


## Hierarchical bayesian model {#hierarchical-bayesian-model}

E.g.

-   \\(p \sim N(\mu, \tau)\\) describes player-to-player variability in natural ability to hit, which has a mean \\(\mu\\) and standard deviation \\(\tau\\).
-   \\(Y \mid p \sim N(p, \sigma)\\) describes a player's observed batting average given their ability \\(p\\), which has a mean \\(p\\) and standard deviation \\(\sigma=\sqrt{p(1-p) / N}\\). This represents variability due to luck.

Look at what we just did, in urn model, we would have \\( p \\) for the unknown ability of a player, yet fixed.
Now, we add a layer where \\( p \\) is a random variable. So we are changing our model to describe the world.

One can interpret \\( p \\) as one would like, and I think there could be multiple interpretations.

-   player-to-player variability in natural ability to hit
-   player-to-player variability in natural ability to hit for the recent year
-   player-to-player variability in natural ability to hit in major league

I.e. We can define our bayesian modeling, because bayesian modeling is loose on defining what our parameter is refering to.


## Bayesian updating {#bayesian-updating}

To understand what bayesian updating is doing, we'll derive the expression for the posterior mean \\( \mathrm{E}(p | Y = y) \\)

Given:

\begin{aligned}
p & \sim N(\mu, \tau^2) \\\\
Y | p & \sim N(p, \sigma^2)
\end{aligned}

we want to compute \\( \mathrm{E}(p | Y = y) \\).

In Bayesian statistics, the posterior distribution of \\( p \\) given \\( Y \\) combines the prior distribution of \\( p \\) and the likelihood of \\( Y \\) given \\( p \\). According to Bayes' theorem, the posterior is proportional to the product of the prior and the likelihood:

\\[
\text{posterior} \propto \text{prior} \times \text{likelihood}
\\]

When the prior and likelihood are both normal distributions, the posterior distribution is also normal, and its mean is a weighted average of the prior mean and the observed value.

Now, let's derive it.

The density functions for the prior and likelihood are:

\begin{aligned}
\text{prior: } & f(p) = \frac{1}{\sqrt{2\pi \tau^2}} \exp\left(-\frac{(p - \mu)^2}{2\tau^2}\right) \\\\
\text{likelihood: } & f(Y | p) = \frac{1}{\sqrt{2\pi \sigma^2}} \exp\left(-\frac{(Y - p)^2}{2\sigma^2}\right)
\end{aligned}

For a given \\( Y = y \\), the posterior density of \\( p \\) is proportional to the product of these:

\begin{aligned}
f(p | Y = y) & \propto f(p) \cdot f(Y = y | p) \\\\
& \propto \exp\left(-\frac{(p - \mu)^2}{2\tau^2}\right) \exp\left(-\frac{(y - p)^2}{2\sigma^2}\right)
\end{aligned}

Combining and completing the square in the exponent (we'll drop the constant factors as they will cancel out when we normalize):

\begin{aligned}
f(p | Y = y) & \propto \exp\left(-\frac{(p - \mu)^2}{2\tau^2} - \frac{(y - p)^2}{2\sigma^2}\right) \\\\
& \propto \exp\left(-\frac{\sigma^2(p - \mu)^2 + \tau^2(y - p)^2}{2\sigma^2\tau^2}\right)
\end{aligned}

To complete the square, we look for an expression of the form \\( (p - a)^2 \\), where \\( a \\) will be the posterior mean we are looking for.

\begin{aligned}
& -\frac{\sigma^2(p^2 - 2p\mu + \mu^2) + \tau^2(y^2 - 2yp + p^2)}{2\sigma^2\tau^2} \\\\
& = -\frac{(\sigma^2 + \tau^2)p^2 - 2(\sigma^2\mu + \tau^2y)p + \sigma^2\mu^2 + \tau^2y^2}{2\sigma^2\tau^2} \\\\
& = -\frac{(\sigma^2 + \tau^2)(p^2 - 2p\frac{\sigma^2\mu + \tau^2y}{\sigma^2 + \tau^2} + (\frac{\sigma^2\mu + \tau^2y}{\sigma^2 + \tau^2})^2) - (\frac{\sigma^2\mu + \tau^2y}{\sigma^2 + \tau^2})^2 + \sigma^2\mu^2 + \tau^2y^2}{2\sigma^2\tau^2}
\end{aligned}

The term \\( \frac{\sigma^2\mu + \tau^2y}{\sigma^2 + \tau^2} \\) is the posterior mean \\( \mathrm{E}(p | Y = y) \\), and it is weighted by the variances of the prior and the likelihood. Rearranging the terms gives us:

\\[
\mathrm{E}(p | Y = y) = \frac{\sigma^2\mu + \tau^2y}{\sigma^2 + \tau^2}
\\]

Define \\( B = \frac{\sigma^2}{\sigma^2 + \tau^2} \\). Then we have:

\\[
\mathrm{E}(p | Y = y) = B\mu + (1 - B)y
\\]

And as previously shown, \\( B \\) (the weight) is given by \\( \frac{\sigma^2}{\sigma^2 + \tau^2} \\). This weight \\( B \\) represents how much the prior information influences the posterior estimate relative to the observed data, which is intuitive: if the observation's variance \\( \sigma^2 \\) is small (meaning we have high confidence in our observation), the posterior estimate will be closer to the observed value \\( y \\); if the observation's variance is large, we rely more on the prior mean \\( \mu \\).

Therefore, \\( \mathrm{E}(p | Y = y) \\) is a linear combination of the prior mean and the observed data, weighted by their respective uncertainties. This is an optimal estimate under the mean squared error criterion when the prior and likelihood are both normal.

If we define:

\\[ Precision(X) = \frac{1}{Var(X)} \\]

\\[
\mathrm{E}(p | Y = y) \\\\
= \frac{\text{Prior precision}}{\text{prior precision + Likelihood precision}}\mu + \frac{\text{Likelihood precision}}{\text{Prior precision + Likelihood precision}}y
\\]

\\[ \text{Posterior Precision} = \text{Prior Precision} + \text{Likelihood Precision} \\]


## why divide by N-1 not N {#why-divide-by-n-1-not-n}

1.  ****Definition of Variance:**** The population variance \\(\sigma^2\\) is defined as:

       \\[ \sigma^2 = E\left[(X - \mu)^2\right] \\]
    where \\(\mu\\) is the population mean and \\(X\\) is a random variable representing an observation from the population.

2.  ****Sample Variance using Population Mean:**** If we knew the population mean \\(\mu\\), we would calculate the variance using:

    \\[ \sigma^2 = \frac{1}{N}\sum\_{i=1}^N (X\_i - \mu)^2 \\]
    The expected value of this is \\(\sigma^2\\) because we're using the true mean.

3.  ****Sample Variance using Sample Mean:**** In reality, we use the sample mean \\(\overline{X}\\) because we don't know \\(\mu\\):

    \\[ s^2 = \frac{1}{N-1}\sum\_{i=1}^N (X\_i - \overline{X})^2 \\]

4.  ****Bias of an Estimator:**** An estimator is unbiased if its expected value equals the parameter it is estimating. For the sample variance, we want:

    \\[ E(s^2) = \sigma^2 \\]

5.  ****Proof of Unbiasedness:****

    -   First, we recognize that the sum of squared deviations from the true mean can be expressed as a sum of squared deviations from the sample mean plus the square of the deviations of the sample mean from the true mean, adjusted by the sample size:

    \\[ \sum\_{i=1}^N (X\_i - \mu)^2 = \sum\_{i=1}^N (X\_i - \overline{X})^2 + 2(X\_i - \overline{X})(\overline{X} - \mu) + (\overline{X} - \mu)^2 = \sum\_{i=1}^N (X\_i - \overline{X})^2 + N(\overline{X} - \mu)^2 \\]

    -   Taking expectations on both sides and using the linearity of expectation, we have:

    \\[ E\left[\sum\_{i=1}^N (X\_i - \mu)^2\right] = E\left[\sum\_{i=1}^N (X\_i - \overline{X})^2\right] + NE\left[(\overline{X} - \mu)^2\right] \\]

    -   We know that \\(E\left[\sum\_{i=1}^N (X\_i - \mu)^2\right] = N\sigma^2\\) and that \\(E\left[(\overline{X} - \mu)^2\right]\\) is the variance of the sample mean, which is \\(\frac{\sigma^2}{N}\\).

    -   Substituting these values in, we get:

    \\[ N\sigma^2 = E\left[\sum\_{i=1}^N (X\_i - \overline{X})^2\right] + N\frac{\sigma^2}{N} \\]

    -   Simplifying this, we have:

    \\[ N\sigma^2 = E\left[\sum\_{i=1}^N (X\_i - \overline{X})^2\right] + \sigma^2 \\]

    -   Rearranging, we find that:

    \\[ E\left[\sum\_{i=1}^N (X\_i - \overline{X})^2\right] = (N-1)\sigma^2 \\]

    -   This is the expected value of the sum of squared deviations from the sample mean. To get an unbiased estimator of the variance, we divide this by \\(N-1\\), which gives us \\(E(s^2) = \sigma^2\\).

The key part of the proof is showing that \\(E\left[\sum\_{i=1}^N (X\_i - \overline{X})^2\right]\\) is \\((N-1)\sigma^2\\), and the unbiased estimator of variance comes from dividing this by \\(N-1\\), not \\(N\\).


## Kalman filter and bayesian updating {#kalman-filter-and-bayesian-updating}

Both the Kalman filter and Bayesian updating in hierarchical models use similar mathematical structures to update beliefs based on new information. Let's delve a bit deeper into the math behind both processes.

****Kalman Filter****

The Kalman filter is used in linear state-space models where the state of the system at time \\( t \\) (denoted as \\( x\_t \\)) is estimated from the state at time \\( t-1 \\) and the current observation \\( y\_t \\). The key equations for the update step of the Kalman filter are:

1.  ****Prediction Step****:
    \\[
       \hat{x}\_{t|t-1} = F\_t \hat{x}\_{t-1|t-1} + B\_t u\_t
       \\]
    \\[
       P\_{t|t-1} = F\_t P\_{t-1|t-1} F\_t^T + Q\_t
       \\]

2.  ****Update Step****:
    \\[
       K\_t = P\_{t|t-1} H\_t^T (H\_t P\_{t|t-1} H\_t^T + R\_t)^{-1}
       \\]
    \\[
       \hat{x}\_{t|t} = \hat{x}\_{t|t-1} + K\_t (y\_t - H\_t \hat{x}\_{t|t-1})
       \\]
    \\[
       P\_{t|t} = (I - K\_t H\_t) P\_{t|t-1}
       \\]

Here, \\( F\_t \\) represents the state transition model, \\( B\_t \\) represents the control-input model, \\( u\_t \\) is the control vector, \\( Q\_t \\) is the process noise covariance, \\( H\_t \\) is the observation model, \\( R\_t \\) is the observation noise covariance, and \\( K\_t \\) is the Kalman gain.

****Bayesian Hierarchical Models****

In Bayesian statistics, we often have a similar structure where we update our estimates of parameters based on prior distributions and new observations. The key equation for updating the estimate of a parameter \\( p \\) based on new data \\( y \\) can be represented as:

\\[
\text{Posterior} \propto \text{Likelihood} \times \text{Prior}
\\]

In the case of the hierarchical model you presented, where both \\( p \\) and \\( Y | p \\) are normally distributed, the posterior distribution of \\( p \\) given an observation \\( y \\) is also normal, with mean \\( E(p|Y=y) \\) and some variance. The mean can be derived as a weighted combination of the prior mean and the observed data:

\\[
E(p|Y=y) = B\mu + (1-B)y
\\]

where \\( B \\) is the weight that balances the prior belief and the new evidence.

****Mathematical Comparison****

Both methods involve an update that is a weighted average of prior information and new data. In the Kalman filter, the weights are derived from covariance matrices of the errors (Kalman gain), while in the Bayesian update, the weights are based on the variances of the prior and the data (often encapsulated in precision, which is the inverse of variance).

1.  In both methods, the weight given to the new data decreases as the certainty (or precision) of the prior estimate increases.

2.  Both methods can be seen as minimizing some form of error or variance. The Kalman gain is chosen to minimize the a posteriori error covariance, while in Bayesian updating, the posterior variance is a function of the prior variance and the data variance.

3.  The Kalman filter can be derived from Bayesian principles under the assumption of linear-Gaussian models, where the state transitions and observations are both linear functions with Gaussian noise.

In summary, while the contexts and specific applications of Kalman filters (often in control systems and time-series analysis) and hierarchical Bayesian models (commonly in statistical inference) are different, the underlying mathematical principles are quite similar and revolve around optimally integrating new information with prior beliefs.


## KL divergence and bayesian updating {#kl-divergence-and-bayesian-updating}

In the context of Bayesian updating:

1.  \\( P(\theta) \\) is the prior belief about the distribution of \\( \theta \\).
2.  \\( P(D | \theta) \\) is the likelihood of observing the data \\( D \\) given \\( \theta \\).
3.  \\( P(\theta | D) \\) is the posterior belief about the distribution of \\( \theta \\) after observing \\( D \\).

The true distribution \\( P \\) is unknown, and \\( Q \\) represents a family of distributions from which we're trying to pick the best candidate as our posterior.

The KL divergence from the true distribution \\( P \\) to an approximate distribution \\( Q \\) is given by:

\\[
D\_{\text{KL}}(P || Q) = \int P(\theta) \log\left(\frac{P(\theta)}{Q(\theta)}\right) d\theta
\\]

However, we cannot calculate this directly because \\( P \\) is unknown. Instead, we minimize the divergence by maximizing the posterior probability \\( Q(\theta | D) \\), or more practically, its logarithm (because logs transform products into sums and are more manageable). This is where we introduce a bit of a simplification for illustration purposes.

When we write \\( \max\_Q \log Q(\theta | D) \\), it's shorthand for maximizing the posterior \\( Q \\) with respect to its parameters. It's a way of saying "choose the parameters for \\( Q \\) that make \\( \log Q(\theta | D) \\) as large as possible." In other words, we're looking for the shape of \\( Q \\) that best explains the observed data \\( D \\).

Let's rewrite Bayes' Theorem:

\\[
Q(\theta | D) \propto P(D | \theta) P(\theta)
\\]

Taking logs (and ignoring the normalization constant for the moment):

\\[
\log Q(\theta | D) \propto \log P(D | \theta) + \log P(\theta)
\\]

We maximize this quantity with respect to \\( \theta \\), which is equivalent to minimizing the negative of this quantity, which can be interpreted as a loss function. Thus, when we perform Bayesian updating, we're implicitly solving an optimization problem:

\\[
\theta^\* = \arg \max\_\theta \left( \log P(D | \theta) + \log P(\theta) \right)
\\]

This is where we draw the connection between Bayesian updating and optimization. We "maximize" \\( Q \\) by finding the \\( \theta^\* \\) that gives us the highest posterior probability after observing the data \\( D \\).


## Variational Inference (VI), and bayesian updating {#variational-inference--vi--and-bayesian-updating}

\\[
\text{ELBO}(Q) = E\_{Q}[\log P(D, \theta)] - E\_{Q}[\log Q(\theta | \lambda)]
\\]

Here, \\( P(D, \theta) \\) is the joint probability of the data and the parameters, which can be decomposed into \\( P(D | \theta)P(\theta) \\), where \\( P(D | \theta) \\) is the likelihood of the data given the parameters (not the other way around), and \\( P(\theta) \\) is the prior over the parameters.

The ELBO is used because it is equal to the log marginal likelihood \\( \log P(D) \\) minus the KL divergence between the variational distribution \\( Q(\theta | \lambda) \\) and the true posterior \\( P(\theta | D) \\):
\\[
\log P(D) = \text{ELBO}(Q) + D\_{\text{KL}}(Q(\theta | \lambda) || P(\theta | D))
\\]

The goal in VI is to maximize the ELBO with respect to the variational parameters \\( \lambda \\), which indirectly minimizes the KL divergence because the log marginal likelihood \\( \log P(D) \\) does not depend on \\( \lambda \\) and thus serves as a constant with respect to the optimization.

So in VI, the ELBO serves as a surrogate objective function that is easier to optimize, and it also provides a lower bound to the log marginal likelihood, which is why it's named as such.

Both Bayesian updating and Variational Inference (VI) aim to approximate the true posterior distribution, \\( P(\theta | D) \\), but they approach the problem differently.

Bayesian updating uses Bayes' theorem to directly compute the posterior distribution by updating the prior with the likelihood of the observed data. This is often computationally infeasible for complex models, which is where VI comes into play.

Variational Inference offers an alternative by turning the problem into an optimization problem. Here’s a comparison of the two approaches:

****Bayesian Updating:****

-   Directly calculates the posterior \\( P(\theta | D) \\) using Bayes’ theorem.
-   Is often computationally intensive, especially with large datasets or complex models.
-   The goal is not framed as an optimization problem but as a calculation based on probability rules.

****Variational Inference:****

-   Approximates the posterior \\( P(\theta | D) \\) by finding a simpler distribution \\( Q(\theta | \lambda) \\) that is closest to the true posterior in terms of KL divergence.
-   Converts the problem of computing the posterior into an optimization problem, where the objective is to maximize the ELBO.
-   The KL divergence \\( D\_{\text{KL}}(Q(\theta | \lambda) || P(\theta | D)) \\) is minimized indirectly by maximizing the ELBO.

The key takeaway is that both methods are looking to understand the posterior distribution \\( P(\theta | D) \\), but VI is designed to find a tractable approximation through optimization, making it more suitable for complex or large-scale problems where exact Bayesian methods are not computationally feasible.


## Meta-Bayesian Analysis {#meta-bayesian-analysis}

Bayesian thinking , started by letting go of the notion of frequentiestic true probability at start (prior reflects this)
then somehow, it connects back to the true priority, (not just posterior, but if we think the limit of posterior, it is true priority, and we can think of bayesian updating is going toward that true P)

and i was thinking, what if we make another layer, .. by treating our true posterior, as starting point, and start from it.
then, we might have a new view on what bayesian updating is doing..

and .. yes it might be possible to view it as an attempt to see 'what updating process' is better..
or if there's alternative..

It's like, we can't understand something unless we make the thing we try to understand as part of something, ..
so we make model to understand the part
then .. we question the model, what it means, it requires another layer (bigger system) to give meaning to the model..

At this level, one might analyze the updating process itself. We could have a distribution over possible priors or even over possible updating rules. This would involve having beliefs about the structure of the Bayesian updating process and the priors that are used. It's reflective and reflexive, examining the process by which we refine our models.


## Nate silver {#nate-silver}

This would be bayesian updating version of Nate silver's aggregation strategy.

```python
import pandas as pd
from scipy.stats import norm
import pyreadr
import numpy as np

# Assuming you have the 'polls_us_election_2016' DataFrame already loaded in Python
# You can read data in Python using `pd.read_csv('file_name.csv')` or other similar functions

result = pyreadr.read_r('polls_us_election_2016.rda')
polls_us_election_2016 = result['polls_us_election_2016']

date_cutoff = pd.to_datetime("2016-10-31").date()

# Filter the data
polls = polls_us_election_2016[
    (polls_us_election_2016['state'] == "U.S.") &
    (polls_us_election_2016['enddate'] >= date_cutoff) &
    (polls_us_election_2016['grade'].isin(["A+", "A", "A-", "B+"]) | polls_us_election_2016['grade'].isna())
]

# Mutate to add a new column for spread
polls['spread'] = polls['rawpoll_clinton']/100 - polls['rawpoll_trump']/100

# Get one poll per pollster
one_poll_per_pollster = polls.groupby('pollster').apply(lambda x: x[x['enddate'] == x['enddate'].max()]).reset_index(drop=True)

se = np.std(one_poll_per_pollster.spread, ddof=1) / np.sqrt(one_poll_per_pollster.shape[0])
mean = np.mean(one_poll_per_pollster.spread)


# Bayesian updating
mu = 0
tau = 0.035
# sigma = results['se']
sigma = se
Y = mean
B = sigma**2 / (sigma**2 + tau**2)
posterior_mean = B * mu + (1 - B) * Y
posterior_se = np.sqrt(1 / (1 / sigma**2 + 1 / tau**2))

# 95% credible interval
credible_interval = posterior_mean + norm.ppf([0.025, 0.975]) * posterior_se

# Probability of d > 0
probability_d_greater_than_0 = 1 - norm.cdf(0, posterior_mean, posterior_se)
print(probability_d_greater_than_0)

# our Y = d + error
# we introduce more uncertainty
# Y = d + b + error
# Here b is a random variable that accounts for the election-to-election variability. This random variable changes from election to election, but for any given election, it is the same for all pollsters and polls within on election.
# and we assume it has variance 0.025

sigma = np.sqrt(se**2 + 0.025**2)
B = sigma**2 / (sigma**2 + tau**2)

posterior_mean = B * mu + (1 - B) * Y
posterior_se = np.sqrt(1 / (1 / sigma**2 + 1 / tau**2))

# Probability that the posterior mean is greater than 0
prob_greater_than_zero = 1 - norm.cdf(0, posterior_mean, posterior_se)

print(prob_greater_than_zero)



```


## Conjugate prior {#conjugate-prior}

A conjugate prior is a choice of prior distribution that, when combined with the likelihood function, results in a posterior distribution that is in the same family as the prior probability distribution.

This doesn't say the conjugate prior is the correct prior for the likelihood function. It just makes math easier.

Nomal distribution is a conjugate prior for a normal distribution, as shown in deriving \\( B \\) for the normal distribution.


### Beta is conjugate prior to Binomial {#beta-is-conjugate-prior-to-binomial}

Binomial:

\\[ P(X = x) = \binom{n}{x} p^x (1 - p)^{n - x} \\]

Beta:

\\[ f(p; \alpha, \beta) = \frac{p^{\alpha - 1} (1 - p)^{\beta - 1}}{B(\alpha, \beta)} \\]

Find a posterior dist \\( p|X \\) for a binomial \\( X|p \sim Bin(n,p) \\) and conjugate prior \\( p = Beta(a, b) \\)

\\[ f(p |X=k) =P(X=k|p) f(p) \\]

\\[ \propto p^{a+k-1} (1-p)^{b+n-k-1} \sim Beta(\alpha + k, \beta + n- k )\\]

When you had prior \\( \alpha - 1\\) sucess and \\( \beta - 1\\) failures, bayesian update with \\( k \\) success and \\( n-k\\) failure, you get the .. new beta distribution.


#### Beta as distribution of p of binomial {#beta-as-distribution-of-p-of-binomial}

\\[ P(X=k) = \int \binom{n}{k} x^{k} (1-x)^{n-k} dx = \frac{1}{n+1} \\]

can be interpreted as the probability of # of white balls which lands left to a white ball.
where you throw n+1 balls into [0, 1] line, all white and 1 pink.

You think of two stories (Baye's Billiards) :

1.  color pink ball and throw them.
2.  throw them and pick a ball and color it as pink

    Then, you get either 0 or upto n balls to the left with equal probability.
    \\[ P(X = k) = \int P(X=k|p) f(p) dp \\]

So the beta distribution can be thought as a distribution of p which will give us \\( P(X = k) \\) for k. (assuming \\( f(p) = 1 \\) i.e. uniform which is also a beta distribution. so it's self reflexive)


## T distribution {#t-distribution}

Sum of many random variables follow normal distribution. Why are we using T?
Because the sample size is small and we are using the SE as an estimate for \\( sigma \\), our sample is not actually a normal, but closer to T.

1.  ****Sample Mean (\\( \bar{X} \\)) Distribution****:

    The sample mean of a random sample drawn from a normal distribution with mean \\( \mu \\) and variance \\( \sigma^2 \\) is also normally distributed with mean \\( \mu \\) and variance \\( \sigma^2/n \\):

    \\[ \bar{X} \sim N\left(\mu, \frac{\sigma^2}{n}\right) \\]

2.  ****Sample Variance (\\( s^2 \\)) Distribution****:

    The sample variance \\( s^2 \\) is related to the chi-squared distribution. If \\( X\_i \\) are independent normal random variables, then \\( (n-1)s^2/\sigma^2 \\) (where \\( s^2 \\) is the sample variance) follows a chi-squared distribution with \\( n-1 \\) degrees of freedom:

    \\[ \frac{(n-1)s^2}{\sigma^2} \sim \chi^2\_{n-1} \\]

3.  ****Combining the Two****:

    To form the t-statistic, you're essentially normalizing the sample mean by the estimated standard error of the mean, which is the sample standard deviation divided by the square root of the sample size (\\( s/\sqrt{n} \\)):

    \\[ T = \frac{\bar{X} - \mu}{s/\sqrt{n}} \\]

    This can be rewritten as:

    \\[ T = \frac{\bar{X} - \mu}{\sigma/\sqrt{n}} \cdot \frac{\sigma}{s} \\]

    Here, the first fraction \\( (\bar{X} - \mu)/(\sigma/\sqrt{n}) \\) would follow a standard normal distribution (Z-distribution) if \\( \sigma \\) was known. Since \\( \sigma \\) is unknown and we use \\( s \\) instead, we need to account for the additional variability introduced by estimating \\( \sigma \\) with \\( s \\). This is done by multiplying by \\( \sigma/s \\), which introduces the second distribution, the square root of a chi-squared distribution (because \\( s^2 \\) is involved), into the mix.

4.  ****t-Distribution Derivation****:

    The t-distribution arises when you divide a standard normal variable \\( Z \\) by the square root of a chi-squared variable \\( X^2 \\) divided by its degrees of freedom, which is independent of \\( Z \\):

    \\[ T = \frac{Z}{\sqrt{X^2/(n-1)}} \\]

    Here, \\( Z \\) has a standard normal distribution, and \\( X^2 \\) has a chi-squared distribution with \\( n-1 \\) degrees of freedom. The resulting distribution of \\( T \\) is the t-distribution with \\( n-1 \\) degrees of freedom.

5.  ****Non-Normality of the t-Distribution****:

    The t-distribution is not normal because the denominator introduces variability from the chi-squared distribution. This means that for small samples, the distribution of the t-statistic has fatter tails than the normal distribution, reflecting the additional uncertainty from estimating \\( \sigma \\) with \\( s \\). As the sample size gets larger, the chi-squared distribution in the denominator becomes more concentrated around its mean (which is its degrees of freedom), and thus the t-distribution approaches a normal distribution due to the law of large numbers.

    The critical takeaway is that the t-distribution accounts for the additional uncertainty that comes with estimating the population variance from a sample, especially when that sample is small. This is why it has heavier tails compared to the normal distribution, indicating a higher probability of observing values far from the mean.


### Interpretation {#interpretation}

T is our best unbiased against true mean / variance, when we have not big enough sample size, to .. approximate our probabilites .. provided that, if we want to model our probability distribution approaches to normal as n goes to infinity.

so in this sense, T is an estimator or .. approximator for N . ie it is the best random variable we can model which would go to N as n goes to infty

\\[ T = \frac{Z}{\sqrt{X^2/(n-1)}} \\]

Here, it is not trivial to see \\( Z \\) and \\( X^2 \\) are independent. After all, they are from the same sample. Yet it turns out they are independent. and it seems to be proven in another theorem. (Cochran's)
