+++
title = "What can be debated?"
author = ["littlehome"]
date = 2023-10-20
lastmod = 2023-10-20T16:50:52+09:00
draft = false
+++

## Q1: Does debate assume an assertion that can be answered yes or no? {#q1-does-debate-assume-an-assertion-that-can-be-answered-yes-or-no}


## What does it mean to ask the Q1 to another person? {#what-does-it-mean-to-ask-the-q1-to-another-person}


## Decidable Statements {#decidable-statements}

Let's consider a formalization of the idea that there exists a statement with a determinate truth value.


### Definitions {#definitions}

-   Let \\( \mathcal{S} \\) be the set of all statements.
-   Define the truth value function \\( \tau: \mathcal{S} \rightarrow \\{0, 1, \text{undefined}\\} \\) such that:
    -   \\( \tau(P) = 1 \\) if \\( P \\) is true.
    -   \\( \tau(P) = 0 \\) if \\( P \\) is false.
    -   \\( \tau(P) = \text{undefined} \\) if \\( P \\) does not have a determinate truth value.


### Main Statement {#main-statement}

The existence of a statement with a determinate truth value can be expressed as:
\\[
   \exists P \in \mathcal{S} \\, : \\, \tau(P) \in \\{0, 1\\}
   \\]

We say P is decidable statement.


## is the definition truely capture the nature of debate? {#is-the-definition-truely-capture-the-nature-of-debate}


## the weakness of the definition {#the-weakness-of-the-definition}


### it assumes the truth value exists for the statement at hand {#it-assumes-the-truth-value-exists-for-the-statement-at-hand}


#### What happens when there's no observable truth value? {#what-happens-when-there-s-no-observable-truth-value}

In extreme case, let's think about the statement "God exists"

Is there a truth value to the question "Does God exist" ?

I don't know the answer.

-   I don't know if it is true or false
-   I don't know if there's a truth value to this question
    -   I don't know if human has capability of answering the question.
    -   I don't know if the notion of God can be defined
    -   I don't know if the word "exist" can be defined
    -   I don't know if this statement belongs to class of statement. ie does P have property of \\( \tau(P) \in \\{0, 1\\} \\)

Then we are not allowed to have a debate on whether "God exists" if we use the definition.

So one can say, we have to be silent on this matter.
But don't we get some values out of the discussion on the question?
Can you assert the question is not debatable? (Do you know for sure if the question can not be answered?)
I say, the act of defining what is debatable defines what the person thinks what debatable is. It doesn't mean there can be alternative definition.


#### it forces us to think of truth value {#it-forces-us-to-think-of-truth-value}

Suppose a question: Is knowledge-a a common sense?
It can be answered yes or no.

But one could argue the is rather inheritantly probablistic, even though people surely associates a boolean value (Yes/No) to the answer.

Ie, assuming truth value forces us to project our probablistic notion to discrete notion without us realizing it.

In another words, when differences arise (such as culture difference, say act of eating dogs), debate forces us to move to true/false dimension from continuous difference dimension.


#### hard to deal with situations when underlying assumption is different {#hard-to-deal-with-situations-when-underlying-assumption-is-different}

When party-a has a statement, party-b might think the statement is not a decidable statement.

It could be that party-b thinks some of assumptions that the statement is assuming is not decidable.

In this case, party-b isn't able to decide yes / no to the statement.
In order to proceed, they have to go over the assumptions of the statement at hand.

But it's often difficult, because the statement itself assumes the decidability and its hard to debate against of the (often hidden or not-self-realized) assumptions


## alternative definition of debate {#alternative-definition-of-debate}

Debate is the communication device where two parties exchange their information on a statement.

Where the debate result can be interpreted as the gained insight on the difference of both parties.


## Probabilistic statement {#probabilistic-statement}


### Definition of Assessment Variables {#definition-of-assessment-variables}

-   Let \\( S \\) be a statement or topic of debate.
-   \\( I\_A \\) is a random variable representing party \\( A \\)'s probabilistic assessment of \\( S \\). Similarly, \\( I\_B \\) represents party \\( B \\)'s probabilistic assessment of \\( S \\).


### Associated Probability Distributions {#associated-probability-distributions}

-   \\( P\_A(x) \\) denotes the probability distribution of \\( I\_A \\), i.e., how party \\( A \\) assigns probabilities to the various outcomes or interpretations of \\( S \\).
-   \\( P\_B(x) \\) denotes the probability distribution of \\( I\_B \\).


### Entropy as a Measure of Uncertainty {#entropy-as-a-measure-of-uncertainty}

The entropy of a random variable quantifies the uncertainty or unpredictability associated with its outcomes. Let \\( H(P) \\) represent the entropy of a probability distribution \\( P \\). Therefore:

-   The entropy of \\( I\_A \\) is given by \\( H\_A = H(P\_A) \\).
-   The entropy of \\( I\_B \\) is given by \\( H\_B = H(P\_B) \\).


### Here object is not to find \\( \tau(P) \\), it is to find the difference {#here-object-is-not-to-find-tau--p--it-is-to-find-the-difference}


#### Difference in Entropies {#difference-in-entropies}

The difference in entropies between the two parties' assessments can be quantified as:
\\[ \Delta H = |H\_A - H\_B| \\]
This difference, \\( \Delta H \\), signifies the relative difference in uncertainty between the assessments of the two parties regarding statement \\( S \\).

eg, how one might measure riskness of an investment position differently from another (ie distribution is different)


#### Difference in Expectation {#difference-in-expectation}

It is the aggregate measurement of observable in a distribution.

eg, what's one's expectation on return on an investment?


#### the entire probability distribution {#the-entire-probability-distribution}

Here one learns about probability distribution of another party.
eg, how one assigns the risk on each possible scenario


#### how one stands different from another {#how-one-stands-different-from-another}

where one can access another party's standing on the shared distribution
eg, based on risk distribution, one might consider a certain risk value to be too risky whereas another might consider it moderate risk.


### changing my base assumption is good thing {#changing-my-base-assumption-is-good-thing}

When a person asks a question assuming yes / no, when he gets answer that it can't be answered that way, or has to be framed differently, he's actually getting much more information than he expected.

Where he expected to measure the strength of Yes / No in a domain, he's getting the probability distribution itself needs change.

So when I ask a question what do you think? if someone answers something completely different, it indicates the possiblity of huge information for me.


## Is one perspective better or truther than another? {#is-one-perspective-better-or-truther-than-another}

How you define 'debate' defines your perspective in some sense.
