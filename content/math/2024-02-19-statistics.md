+++
title = "The Art of statistic, learning from data"
author = ["eugenekim"]
date = 2024-02-19
lastmod = 2024-02-20T02:22:09+09:00
draft = false
+++

This is reinterpretation of the book, `The Art of statistic, learning from data`.


## What is data {#what-is-data}

An individual has no interpretation in itself in statistics.

It's the relationship to the whole (many individuals) which gives the meaning of an individual.

It is contradictory to another perspective where each individual has an inherent meaning.

-   natural rights
-   properties of human (homo sapience, homo ludens..)

And statistics deals with unknowns. If we know everything about something, if we know it deterministically, statistics don't deal with it.

For an unknown, we attach a measurement (binary, continuous, discrete, `QUESTION`: can there be other measurements?), and we gather lots of individuals with the measurement.
We call it data.


## How to derive meaning from data {#how-to-derive-meaning-from-data}

After seeing many men (data), upon seeing a man of a certain height, you can gauge how tall he is among general population.


## Oh he's short, is he? how certain are you? {#oh-he-s-short-is-he-how-certain-are-you}

Let's assume you have seen random men on earth (this won't be correct, you probably have seen men around in your country, or in your neighbor).

If you have seen 100 of them, you can see the mean \\( m \\) (average) height and the variance \\( s^2 \\) of 100 men.

{{< figure src="/ox-hugo/bell.jpeg" width="300px" >}}

If we plot their count (how many 150-155cm men are there, and so on), we will see bell shaped curve.
When you see a men, you can imagine where his height would be placed in this graph, and it gives you sense of how tall he is. oh he is a bit short or etc.

If you have seen all men on the earth, you can be certain he's in lower 30% or etc.
However since you have not seen all men, how centain can you be?


## I don't know if statistics can tell you that.. {#i-don-t-know-if-statistics-can-tell-you-that-dot-dot}

We have to ask more basic question first.

You've seen 100 men, and you think average height is 170cm. But is it?
How certain can you be?

This can be answered using statistics

With your mean and variance, we can construct a confidence interval \\( (m - 2s, m + 2s) \\). We say, we are 95% confident that this interval contains the man's average height.

What does that mean?
It's saying, if you happend to have met different 100 men, many times, 95% of the case of the same procedure would contain the actual men's height average.

See, it's not easy to answer how certain you can be about the judgement on a man's height because we can't even be sure where the true average height is.


## You need random data {#you-need-random-data}

Suppose, you met 100 men in your school.
Trying to find average man height of earth from schoolmate's height won't be accurate.

A lot of poll prediction fails because it's hard to get random sample.


## Predicting from a feature {#predicting-from-a-feature}

Suppose you prefer a taller men because you predict a taller child if you happen to marry him.

We can plot (father height, child height)

{{< figure src="/ox-hugo/Screenshot 2024-02-19 at 11.55.12 PM.png" width="300px" >}}

After plotting the data (draw the dots), we want to simplify the data.
Simplifying data is done through a model.

A model captures a part of the whole data. If you remember, data is only a part of a whole story. I.e. a man is represented as a single number, height.

Here, our model is a line which is representative of the dots.
There could be many ways to choose a representative line.

The line is not the diagonal, angle \\( 45^o\\). I.e. if 10cm taller man doesn't produce 10cm taller child, slightly shorter than that, and 10cm smaller man produce slighlty taller than -10cm. Hence the term, regression to the mean.


### what is a statistical model {#what-is-a-statistical-model}

After drawing the line, we can claim (or imagine) that each dot is comprised of the deterministic part where the line is, and the risidual error (the distance from the line to each dot)

Alternatively, a data can be interpreted as signal and noise.

If you look closely, signal is not some a holy axiom that's supposed to be found, it's just our mental projection using a model that we want to treat as a base line.

So one can call it, basis and deviation, or whatever. Just wanna mention the term signal and noise has the connotation that we are dealing with an object truth which is to be found.
It may be in certain cases, and it might not.


## Causation {#causation}

Does father's height cause the child's height?

A father's height is mearly associated with the child's height.

But we feel the causation why?
Because our brain is the casuation machine. It likes to create causation link between events.


### What is causation? {#what-is-causation}

It's hard to define as it's hard to define what love is.

The most accepted (?) definition is based on counter-factual.

I jammed my thumb in the car door, now it hurts.
I suspect jamming my thumb causes the pain.

How do I know? If I haven't jammed my thumb, it wouldn't have hurt.

But we can't unwind the history, we can't test the counter-factual 'not jamming my thumb'.

It's often hard to apply this definition in statistical context.

So, statistical causation (my word) is based on RCT.

If a random sample shows a association, we allow to call it causation.

For instance, if we happen to sample random fathers for the height, and see the association of the child's height, we say a taller farther causes a taller child.

Whereas, association from non random sample might have confounder which can explain the explanation of the association, and we don't call it a causation.

For example, height and weight of a child is strongly correlated, but the association might be explained by the age of the child.


## Accuracy of prediction (algorithm) {#accuracy-of-prediction--algorithm}


### `Question` How to tell the accuracy of regression (prediction of a numeric value)? {#question-how-to-tell-the-accuracy-of-regression--prediction-of-a-numeric-value}


### Classifier accuracy {#classifier-accuracy}


#### Accuracy {#accuracy}

How often an algorithm is right in prediction? High accuracy can be deceiving.


#### ROC, AUC {#roc-auc}

ROC curve and AUC is measures the algorithm performance.

ROC is the plot of sensitivity (TPR) and (1-specificity) (FPR) over varying threshold.

sensitivity: probability of finding a guilty person as guilty
specificity: probability of finding a innocent person as innocent

AUC is the area under ROC curve, and it has a nice interpretation.
Given a random guilty person and a random innocent person, the algorithm has a probability of AUC (e.g. 80%) to assign higher score for the guilty person than the innocent person. (It is the expected probability over all threshold)

<!--list-separator-->

-  proof

    \\[ FPR(T): T \\rightarrow x \\]
    \\[ TPR(T): T \\rightarrow y(x) \\]

    \\[ A = \\int_{x=0}^{1} TPR(FPR^{-1}(x)) \\, dx \\]

    Change of variable: \\( dx = FPR'(T) \\, dT \\)

    \\[ A = \\int_{T} TPR(T) \\cdot FPR'(T) \\, dT \\]

    Let \\( f_1(T) \\) be the probability density function (PDF) for the scores of the positive instances.

    Let \\( f_0(T)\\) be the probability density function (PDF) for the scores of the negative instances.

    \\[ TPR(c) = P(T' &gt; c) \\]
    \\[ FPR(c) = P(T &gt; c) \\]

    I.e. TPR is CDF of \\( f_1 \\) and FPR is CDF of \\( f_0 \\).

    Now,

    \\[ A = \\int_{-\\infty}^{\\infty} \\int_{-\\infty}^{\\infty} I(T' &gt; T)f_1(T')f_0(T) \\, dT' \\, dT \\]

    -   The integral of \\( TPR(c) \\cdot FPR'(c) \\, dc \\) over all \\( c \\) is the same as calculating the integral of the joint probability \\( f_1(T') \\cdot f_0(T) \\) over all score pairs \\( (T, T') \\) such that \\( T' &gt; T \\).
    -   This is because \\( TPR(c) \\) is the integral of \\( f_1(T') \\) over all \\( T' &gt; c \\), and \\( FPR'(c) \\) is \\( f_0(c) \\).

    And, \\( A = P(X_1 \\geq X_0) \\), where \\( X_1 \\) is the score for a positive instance and \\( X_0 \\) is the score for a negative instance


#### Alpha, Beta {#alpha-beta}

-   Type-1 error (Alpha): We don't want to blame innocent person as guilty (alpha=5%, we only allow 5% mistake)
-   Type-2 error (Beta): Finding someone not guilty when he acutally commited crime
-   Power of a test := 1 - Beta: Correctly calling a guilty person as guilty.

Once you set a desired error rate, you can find the neccessary sample size.

`Question` Can you apply this to the judgement accuracy of man's height problem?


## Bayes {#bayes}


### Initial likelihood {#initial-likelihood}

Suppose, you visited Mars, and found a man, and he's tall. Now you wanna date him because he is tall.
But alas, he might be a dwarf on Mars. Martitian might be much taller than earthlings.

The initial response is based on previous data. As you meet more martitians, you can update your expectation on martitian's height.

`Question` How much should I give weight to my previous data on earth men?

Would it be better to use earthling's height data on predicting martitian's height? Maybe not, but if we are to predict a universal man's height, it probably is better to use it.


### Inverse condition {#inverse-condition}

Suppose you are doing a doping test. Your test is 95% accurate, for dopers and non-dopers. 1 in 50 atheletes are truly doping at any time. If an athelete tests positive, what's the probability that he's truly doping.

A temporal order is,

-   whether an athelete does dope or not
-   doping test positive or negative

We change the order of reasoning backward to:

A temporal order which we come to know things

-   doping test positive or negative
-   whether an athelete did dope or not

I.e. if an athelete tests positive, what's the probability that he's truly doping?

This is `epistemic` probability. He either doped or not, but we merely don't know, so we are assigning a probability on our judgement.

Whereas the probability of test positive of a given person is `aleatory` probability.

If we have another way of telling whether he doped or not, we could also use that to update the probability on our judgement. So you can learn from experience how the world works step by step using bayes.


#### Solution to the problem using bayes {#solution-to-the-problem-using-bayes}

the initial odds for the hypothesis \* the likelihood ratio = the updated odds for the hypothesis

(1 / 49) \* (0.95 / 0.05) = 19 / 49 (odds)

So the probability is 19 / (19+49)

Or you can get the same solution using inversed tree.
