+++
title = "Linearity"
author = ["littlehome"]
date = 2023-10-13
lastmod = 2023-10-16T16:39:49+09:00
draft = false
+++

## linearity {#linearity}

<https://chat.openai.com/share/1d1f168c-0009-4906-b451-bc77dce64dc9>


### what is linearity (in linear algebra) {#what-is-linearity--in-linear-algebra}

There is a mapping from an object to another object (from v to w)

two objects can be added and we can look at the mapping of the resulting object
the mapping is linear when T(v1 + v2) = T(v1) + T(v2)

(there's an additional homogeneous requirement as well
and there is assumption where v is an entity of vector space with some additional conditions (such as property of +, + identity and so on)

As discussed in the chat, function composition is not a proper vector space addition operator.
So differentiation on function composition (chainrule) is not additive.


### why linearity of expectation holds even when random variables are dependent {#why-linearity-of-expectation-holds-even-when-random-variables-are-dependent}

The universe of X2 does exist independently from the universe of X1.

This statement says what kind of assumptions we are making on the subject of random variable we study. Namely, the distribution is fixed even if we might not be aware of what it looks like.

I'm saying, the mathematical property we assume is fixed as in Platon's idea.
Not because that is true but because that is our assumption. ie, we are not considering where one variable might change the distribution of another. We assume those are already baked in every distribution

Suppose X1, X2 is palyer1, player2's score (table tennis)

E(X1 + X2) = E(X1) + E(X2)
is it?

Of course it's not something provable. Because we don't know the true distribution of the X1 and X2.
It is our model that X1 and X2's distribution is fixed.
But whether X1 meet X2 and be a team partner will have impact on their score.

Whether player1's score in his whole life will depend on whether he will be teamed up with.
Our mathematical model, consider both cases of X1, X2's being teamed up and not being teamed up, and it's expectation has those property.
I can't argue that reasoning is falsy, but i'm saying that's not provable in many cases such as this.
Or I could argue, we need diferent way of defining random variable if we want to model one random variable can change another variable's distribution.(then the linearity of expectation might not hold)
