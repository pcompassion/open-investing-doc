+++
title = "Derivative Game"
author = ["김유진"]
date = 2023-11-17
lastmod = 2023-11-18T21:07:13+09:00
draft = false
+++

## Game {#game}

A game host has a convert ticket whose price is determined by supply and demand of the game players.. (He has many tickets for the same concert)
He invites you to play the game which ends a week later.

You can bet on price movement, if you get it right, you can make money.


### Specifically, you can take an action of the followings: {#specifically-you-can-take-an-action-of-the-followings}

-   If you think the price will rise:

    You tell the host you think the price will rise.

    The host and you agree that if price in the future actually rises, you earn the difference, if price falls, you lose the difference.

    The host and you makes an agreement paper which says:
    You are going to buy the concert ticket at price F a week later. (F is the market price at the time of the agreement)

    So now, if price in the future is equal to price F, you gain nothing.
    However, if the price rise above F, you make money and lose if price ends up below F

-   if you think the price will fall:

    You and the host makes an agreement:

    You are going to sell the concert ticket at price F a week later. (F is the market price at the time of the agreement)

    So now, if the price rise above F, you lose money and you make money if price ends up below F


### In summary {#in-summary}

-   when you think price will rise: You buy it. (You agree to buy it with current market price in the future.)
-   when you think price will fall: You sell it. (You agree to sell it with current market price in the future.)


### You can take the above actions as many as you want. {#you-can-take-the-above-actions-as-many-as-you-want-dot}


### You can also exit the game early by taking an opposite action. {#you-can-also-exit-the-game-early-by-taking-an-opposite-action-dot}

Suppose you made a guess that price will rise in the past.

Now you think the price will fall from now on.
So you go and make another agreement, that you want to sell.

Now you have agreement to buy the ticket and also to sell the ticket in the future.

If your selling price is higher than your buying price, you gain, otherwise you lose.
And your outcome is actually already known, and you don't have to wait for the game to finish.

****QUESTION****

The price difference is in the future, how the host give you the money or take the money in the present time?

Does he apply interest rate? or because it's so short, we are ignoring it?, then the game is rigged!..


#### Once you have the both side of the trade, i.e. buy and sell, you are effectively done playing the game. {#once-you-have-the-both-side-of-the-trade-i-dot-e-dot-buy-and-sell-you-are-effectively-done-playing-the-game-dot}


## Game 2 {#game-2}

Now the host has a new game.

In previous game, if you predict wrong, you lost money.

Now, in this new game, you pay insurance fee, but if you predict wrong, you just lose the insurance fee.
When your prediction is right, you end up paying the insurance fee but it is small compared to the risk that your prediction might be wrong.

So do you host collect the insurance fee? No


### The insurance fee goes to the other player not to the host {#the-insurance-fee-goes-to-the-other-player-not-to-the-host}

When you buy or sell, you have to find a player who would want sell or buy (if you buy, he has to sell)

The insurance fee goes from buyer to seller? No.


### Buyer or seller can play the role of insuerer or insured {#buyer-or-seller-can-play-the-role-of-insuerer-or-insured}

Remember, buy and sell are the prediction you make in the present.

-   insurance company collects the insurance fee, but he can lose big
-   an insured can win big, but loses small


#### 4 types of players {#4-types-of-players}

-   insurer (insurance company) who predicts price rise
-   insured who predicts price fall

-   insurer (insurance company) who predicts price fall
-   insured who predicts price rise


## Fair price {#fair-price}

How players can access the fair price at the present time?

If a player sells a (right-of) ticket at \\( F\_0 \\) at time \\( t\_0 \\) and sells a ticket at \\( F\_T \\) at time \\( t\_T\\). (i.e. He made a comitment to sell.)

And he also buys a ticket at price \\( S\_0 \\) at time \\( t\_0 \\) becomes  \\( S\_T \\) at time \\( t\_T \\)
\\( F\_T = S\_T \\) because at time \\( T \\) the predicted ticket price gets close to the actual ticket price at the time \\( T \\) which is when the game ends.

His total asset is \\( S\_T - S\_0 + F\_0 - S\_T = -S\_0 + F\_0 \\).

Importantly, there's no randomness left in the equation. We have only constants.


### What does it mean? {#what-does-it-mean}

Suppose there are two tickets \\( S\_A \\) and \\( S\_B \\)
Suppose they have the same current market price \\( S\_0 \\) and same game ending date \\( T \\),

Suppose they have different market price for the prediction game. \\( F\_A0 < F\_B0 \\)

****QUESTION**** If one buys \\( S\_0 \\) and sells \\( F\_B0 \\), he's better off than someone who sells \\( F\_A0 \\)

This can't happen. What do you mean can't happen?
The interpretation is that the gain of \\( F\_0 - S\_0 \\) should be equal to the other financial activity which has no randomness such as savings account.

****QUESTION**** What is the assumption of the interpretation?

It assumes that if the assumption is not met, one can instead play the strategy instead of using the savings account without incurring any more risk.

Ok, theoretically makes sense. but can we really apply that model to the real world?
I.e would anyone bet on the interpretation and really use the game strategy over savings account?
Doubtful, but the price \\( F\_0 \\) should not be far from the theoretical model can be understood.

****QUESTION**** what if we buy that assumption, then what's the interpretation?

Suppose you have two tickets which you expect their future price will be the same, but their variance is different.

The model doesn't give any preference to the ticket which smaller variance.

So if we take the model as valid, we are left with the question that any quality (not just variance) of ticket doesn't matter.

Alternatively, one can reason backward: all that quality should be already incorporated in the current price \\( S\_0 \\), so it doesn't violate our common sense.

Now then, it is awkward if we consider, selling the two tickets now, they yield the same benefit to me. (the same price \\( S\_0 \\))
So the alternative interpretation is not explaining away the different quality in the future, because at present time they are truely equal.

So, am I buying that argument that there's a fair price because of the non arbitrage principle?

****QUESTION**** what is the alternative perspective's assumption?

Let us denote the perspective of no arbitrage as P1, and the other questioning perspective as P2.

When P2 have the same 'expectation' \\( F\_T \\) and different variance

P2 are assuming the expectation can be considered as the price in the future.

-   P2: There are products with the same expectation price, but with different variances, we value them differently, yet P1 is saying they should be same.
-   P1: I didn't make that claim. I only talk about current price, and a (fixed) future price. (with no expectation attached)


#### Assumptions on both sides {#assumptions-on-both-sides}

<!--list-separator-->

-  Assumptions of P1 (narative of P2)

    -   You (P1) are saying that different ticket with the same \\( S\_0 \\) and \\( S\_T \\) has the same value whatever path it took from \\( S\_0 \\) to \\( S\_T \\)

    -   You (P1) are saying, when you have the same initial price and ending price, there's no difference (which can be measured by price) between the two tickets.

    -   You are saying, when we have the same price in the present, the price itself and the price alone is indicative of the future value of the product.

        E.g investing in real estate vs investing in stock with the same amount of money should yield the same return. (Despite we sense they have inherently different qualities)

        P1: I'm saying 'savings account' and this 'ticket game' is so easy to move-in and out, its not same as real estate vs stock market.

<!--list-separator-->

-  Assumptions of P2

    -   The world is not that efficient


### So what {#so-what}

It makes sense to reason as P1 does, as the theoretical base.
However, there are so many strong assumptions to use the model.

Not sure how close the model is to the real world.

Of course, if there's a big gap between return on savings account and return on the game market, there will be people who try to profit from the difference and they will close the gaps down.

-   P1's model is (simplification) a perspective to look at only two specific time and price.
-   It's the choice that one choose to reason with that perspective.
    Where one reason from the assumption (or principle) that no arbitrage gain is possible.
    -   It is clear we can not apply the same model to an asset where enter/exit is not so easy.
    -   Buying a ticket and short selling a ticket doesn't cost one much effort. So it is a better candidate to apply the P1 model.
-   I can't buy that the price is already reflecting all the future information.
-   There's no doubt it's a sane model. And I don't know if there can be nicer model yet reflects the reality as well as the P1. Just not sure how close it is.

When we invest on something, we have a different expectation (not just the \\(E\\) but also various qualities). I think that might indicate how far the real world is from the model.
