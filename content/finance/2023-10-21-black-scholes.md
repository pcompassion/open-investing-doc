+++
title = "Black Scholes"
author = ["eugenekim"]
date = 2023-10-21
lastmod = 2023-11-28T01:24:01+09:00
draft = false
+++

## Random walk {#random-walk}

A scenario where the position at the next step is determined by the position at the previous step and the independent outcome of the next coin flip. This is like flipping a coin, where each head means a step forward (+1) and each tail means a step backward (-1). Each step is independent of others and has equal probability.

\\[ \\begin{aligned}
X_i = \\begin{cases}
1 &amp; \\text{with probability } \\frac{1}{2} \\\\
-1 &amp; \\text{with probability } \\frac{1}{2} \\\\
\\end{cases}
\\end{aligned} \\]

Then,

\\[
E[X_{i}] = 0 \\\\
Var[X_{i}] = 1 \\]

Let \\( S_{n} = \\sum_{i}^{n} X_{i} \\), then \\( Var[S_{n}] = n \\)


### linear growth of variance {#linear-growth-of-variance}

We can see that the variance of random walk increases propotionaly with number of steps.


### martingale {#martingale}

Simple Random Walk: at step n, your best guess for step n + k is n
Brownian motion: at time t, expected position in \\( B(t+s) \\) is \\( B(t) \\), ie \\(\\mathbb{E}[B(t+s) | B(t)] = B(t)\\)


## Brownian motion {#brownian-motion}

We want a model where W follows a random walk over time t.

So we need to transfrom the discrete random walk to continuous one.

We consider a unit time (which can be hour, day) has n random work, ie \\( S_{n} \\) with variance 1.

Since CLT says: \\( \\lim_{n \\to \\infty} \\frac{S_{n}}{\\sqrt{n}} = N(0, 1) \\)

We let:
\\[ W_{n}= \\frac{S_{n}}{\\sqrt{n}} \\]
\\[ W = \\lim_{n \\to \\infty} W_{n} \\]

Then \\( W \\) stands for continuous random work with variance 1 for a unit time.

Since we saw that the variance of random walk increases propotionally with respect to steps, we expect if we look at random walk of interval t (times the unit time), we expect the variance to be t.

\\[ W_{t} = \\sum_{t} W \\]

or one can think of
\\[ W_{t} = \\lim_{n \\to \\infty} \\frac{S_{nt}}{\\sqrt{n}} \\]

And we indeed get \\( Var(W_{t}) = t \\)

So W<sub>t</sub> is a random walk over time t, with variance 1 for a unit time, and variance increases linearly respect to t.


## Geometric Browninan motion {#geometric-browninan-motion}

\\[ dS = μS dt + σS dB \\]

We express the change of variable S by two terms

-   \\(μS dt\\) : constant rate growth
-   \\(σS dB\\) : random fluctuation


### Constant rate growth {#constant-rate-growth}

Start with a discrete compounding model for growth, where:

\\[ s_{t+dt} = s_{t} e^{u dt} \\]

Then take differences to get an increment in s, ds:

\\[ ds = s_{t+dt} - s_{t} = s_{t} (e^{μ dt} - 1) \\]

Then divide through by dt to get a finite difference approximation of the derivative ds/dt:

\\[ (ds/dt) \\approx s_{t}  \\frac{(e^{\\mu dt} - 1)}{dt} \\]

In the limit as dt approaches 0, the right side converges to s<sub>t</sub> \* μ due to the fact that the derivative of e<sup>&mu; t</sup> with respect to t, evaluated at t=0, is μ.

So you end up with this deterministic differential equation:

\\[ \\frac{ds}{dt} = s_{t} μ \\]
\\[ ds = s_{t} μ dt \\]


### Random fluctuation \\(σS dB \\) {#random-fluctuation--σs-db}

Similarly, this term signifies change in s due to random fluctuation

σ represents the standard deviation of the percentage change of the stock price (S) over 1 unit time.
dB is a random variable with N(0, dt), and it gives the random % change which would occur in a dt time interval.

\\(ds = \\sigma s_{t} dB \\) captures the random percentage change in the s over the interval dt


## Ito's lemma {#ito-s-lemma}

Consider the Taylor expansion for f:

\\[ f(t+dt, W(t)+dW) = f(t, W(t)) + \\frac{\\partial f}{\\partial t} dt + \\frac{\\partial f}{\\partial x} dW + \\frac{1}{2} \\frac{\\partial^2 f}{\\partial x^2} (dW)^2 + ... \\]

Subtracting f(t, W(t)) from both sides gives:

\\[ df = \\frac{\\partial f}{\\partial t} dt + \\frac{\\partial f}{\\partial x} dW + \\frac{1}{2} \\frac{\\partial^2 f}{\\partial x^2} (dW)^2 + ... \\]

Furthermore, since dW has the following mean and variance,

\\begin{align\*}
E[dW] &amp;= 0 \\\\
E[(dW)^2] &amp;= dt
\\end{align\*}



If we set W(t) = S(t):

\\[ df(t, S(t)) = \\frac{\\partial f}{\\partial t} dt + \\frac{\\partial f}{\\partial S} dS + \\frac{1}{2} \\frac{\\partial^2 f}{\\partial S^2} (dS)^2 \\]

Now, if we plug our stock price dynamics:

\\[ dS = \\mu S dt + \\sigma S dB \\]

\\[ df(t, S(t)) = \\frac{\\partial f}{\\partial t} dt + \\frac{\\partial f}{\\partial S} (\\mu S dt + \\sigma S dB) + \\frac{1}{2} \\frac{\\partial^2 f}{\\partial S^2} (\\mu S dt + \\sigma S dB)^2 \\]

Focus on the squared term:

\\[ (\\mu S dt + \\sigma S dB)^2 = \\mu^2 S^2 dt^2 + 2 \\mu \\sigma S^2 dt dB + \\sigma^2 S^2 dB^2 \\]
\\[ E[(dX)^2] = E[\\mu^2 dt^2 + 2\\mu\\sigma dt dB + \\sigma^2 dB^2] = E[\\sigma^2 dB^2] \\text{as dt \\to 0} \\]

\\[ (\\mu S dt + \\sigma S dB)^2 \\approx \\sigma^2 S^2 dt \\]

We get,

\\[ df(t, S(t)) = \\left( \\frac{\\partial f}{\\partial t} + \\mu S \\frac{\\partial f}{\\partial S} + \\frac{1}{2} \\sigma^2 S^2 \\frac{\\partial^2 f}{\\partial S^2} \\right) dt + \\sigma S \\frac{\\partial f}{\\partial S} dB \\]


## Black-Scholes assumption {#black-scholes-assumption}

1.  Stock prices follow a geometric Brownian motion (as constant rate growth and random fluctuation).
2.  No arbitrage opportunities.
3.  The risk-free rate is constant. and every asset return rate is the risk-free rate.
4.  Volatility for a unit time is constant.
5.  There are no taxes or transaction costs.
6.  The option is European, meaning it can only be exercised at expiration.
7.  All investors are indifferent to risk. ie, investors don't mind paying the same price for different


## Option Dynamics {#option-dynamics}

We have,

\\[ dV = \\left( \\frac{\\partial V}{\\partial t} + rS \\frac{\\partial V}{\\partial S} + \\frac{1}{2} \\sigma^2 S^2 \\frac{\\partial^2 V}{\\partial S^2} \\right) dt + \\sigma S \\frac{\\partial V}{\\partial S} dB \\]

In the risk-neutral world, the expected return on the option must also be the risk-free rate. Therefore, the expected change in the option price over a small time interval dt should be rVdt.

\\[ E[dV] = rV dt \\]

\\[ E[dV] = E \\left[ \\left( \\frac{\\partial V}{\\partial t} + rS \\frac{\\partial V}{\\partial S} + \\frac{1}{2} \\sigma^2 S^2 \\frac{\\partial^2 V}{\\partial S^2} \\right) dt + \\sigma S \\frac{\\partial V}{\\partial S} dB \\right] \\]

Now since Since E[dB] = 0,

\\[ \\frac{\\partial V}{\\partial t} + rS \\frac{\\partial V}{\\partial S} + \\frac{1}{2} \\sigma^2 S^2 \\frac{\\partial^2 V}{\\partial S^2} - rV = 0 \\]


## Replicating portfolio {#replicating-portfolio}

We hold a call option:

\\[ \\text{profit} = S(t) - \\text{strike_price (buy price)} \\]

We want to delta hedge by short selling a stock:

\\[ \\text{profit} = \\text{sell_now} - S(t) \\]

Notice that \\(S(t) \\) for call option and short selling  moves to the opposite direction.

We build a portfolio &Pi; consisting of one European call option and a certain number, −Δ, of shares of the stock

1.  Portfolio Construction

    \\[ \\Pi(t, S) = C(t, S) - \\Delta S \\]

2.  Option Dynamics

    We obtained by equating option price change rate to risk-free rate
    \\[ dC = \\frac{\\partial C}{\\partial t} dt + \\frac{\\partial C}{\\partial S} dS + \\frac{1}{2} \\frac{\\partial^2 C}{\\partial S^2} (dS)^2 \\]

3.  Portfolio Dynamics
    Now let's consider the differential change, ie change due to both time and stock price

    \\[ d\\Pi = dC - \\Delta dS \\]

    \\[ d\\Pi = \\left( \\frac{\\partial C}{\\partial t} dt + \\frac{\\partial C}{\\partial S} dS + \\frac{1}{2} \\frac{\\partial^2 C}{\\partial S^2} (dS)^2 \\right) - \\Delta dS \\]

4.  Risk-free Portfolio

    We choose &Delta; such that Portfolio is risk-free. We eliminate the random term dS which represents fluctuation due to stock price change.

    \\[ \\Delta = \\frac{\\partial C}{\\partial S} \\]
    \\[d\\Pi = \\frac{\\partial C}{\\partial t} dt + \\frac{1}{2} \\frac{\\partial^2 C}{\\partial S^2} (dS)^2 \\]

5.  Portfolio return = Risk-free rate

    \\[ \\frac{d\\Pi}{\\Pi} = r dt \\]

    Substituting expressions from step 1, 4

    \\[ \\frac{\\frac{\\partial C}{\\partial t} dt + \\frac{1}{2} \\frac{\\partial^2 C}{\\partial S^2} (dS)^2}{C - \\Delta S} = r dt \\]

6.  Simplify

    By using \\((dS)^2 = \\sigma^2 S^2 dt\\)  (We established (\\(\\mu S dt + \\sigma S dB)^2 \\approx \\sigma^2 S^2 dt \\))
    \\[ \\frac{\\frac{\\partial C}{\\partial t} dt + \\frac{1}{2} \\frac{\\partial^2 C}{\\partial S^2} (dS)^2}{C - \\Delta S} = r dt \\]

    By substituing for &Delta;

    \\[ \\frac{\\partial C}{\\partial t} + rS \\frac{\\partial C}{\\partial S} + \\frac{1}{2} \\sigma^2 S^2 \\frac{\\partial^2 C}{\\partial S^2} - rC = 0 \\]


### No arbitrage principle {#no-arbitrage-principle}

Through the process of delta hedging, we construct a portfolio that is insensitive to underlying stock price change.
Then the return of portfolio should be equal to risk-free rate.


### Same PDE {#same-pde}

PDE derived from option dynamics is equal to PDE derived from no arbitrage principle.
So the PDE satisfies the both dynamics (conditions)

-   option return is equal to risk-free rate
-   no arbitrage principle


## Equation solving {#equation-solving}


### First transformation {#first-transformation}

\\[ V(t,S)=Ke^{-rτ} f(x,τ) \\text{ where } τ = T−t \\text{ and } x = \\ln(\\frac{S}{K}) \\]

We suspect that transformation would help us to solve the equation.

.. skipped..

f(x, 0) = e<sup>x</sup> - 1

\\begin{cases}
e^x - 1 &amp; \\text{if } x &gt; 0 \\\\
0 &amp; \\text{if } x \\leq 0
\\end{cases}

Shows the option value is propotional to % increase of stock price , when expiration.

.. skipped ..


### Second transformation {#second-transformation}

\\[
y = e^{a x} \\\\
\\theta(\\tau, y) = e^{b \\tau} f(x, \\tau)
\\]

Here \\( \\Theta \\) plays the role of u in heat equation.

\\[ u_{t} = u_{xx} \\]

Where, in our case, we have
\\[ \\tau = T - t, y = e^{ax}, x = \\ln \\left(\\frac{S}{K}\\right) \\]

Then we can see, y is linear to S (stock price). So the resulting transformed equation is expressed with scaled version of time and stock price.

u (transformed option price) is related as:
\\[ u_{t} = u_{ss} \\]

Amazing.. so why there's a connection from t to S? ..
I suspect it has to do with our modeling that relates our stock price as random walk, and..

.. skipped ..

We solve the quation and arrives at the closed form solution

\\[ C(S, t) = SN(d_1) - Ke^{-r(T-t)}N(d_2) \\]


## Interpretation {#interpretation}

Let's go back to the Geometric Brownian Motion equation of stock price

\\[ dS_t = \\mu S_t dt + \\sigma S_t dB_t \\]

We apply Ito's lemma to find the differential \\( d\\ln(S_t) \\) by setting \\(f(t, W(t)) = \\ln(S_t) \\)

Since it doesn't directly depend on time, \\(\\frac{\\partial \\ln(S_t)}{\\partial t} = 0 \\)

Additionally
\\( \\frac{\\partial \\ln(S_t)}{\\partial S_t} = \\frac{1}{S_t}, \\frac{\\partial^2 \\ln(S_t)}{\\partial S_t^2} = -\\frac{1}{S_t^2}\\)

Plugging this into Ito's lemma:

\\[ df(t, S_t) = \\left( \\frac{\\partial f}{\\partial t} + \\mu S_t \\frac{\\partial f}{\\partial S_t} + \\frac{1}{2} \\sigma^2 S_t^2 \\frac{\\partial^2 f}{\\partial S^2_t} \\right) dt + \\sigma S_t \\frac{\\partial f}{\\partial S_t} dB_t \\]

Becomes:
\\[d\\ln(S_t) = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) dt + \\sigma dB_t \\]

If we integrate both sides

\\[ \\ln(S_t) - \\ln(S_0) = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) t + \\sigma B_t \\]

So \\( S_{t} \\) is lognormal, because \\( B_{t} \\) is normal.

And alternatively,

\\[ S_t = S_0 e^{\\left( \\mu - \\frac{1}{2}\\sigma^2 \\right) t + \\sigma B_t} \\]

Now we look at the the option price formula as two terms.

\\[ C(S, t) = SN(d_1) - Ke^{-r(T-t)}N(d_2) \\]

\\[ d_1 = \\frac{\\ln \\left(\\frac{S}{K}\\right) + \\left(r + \\frac{\\sigma^2}{2}\\right) \\tau}{\\sigma \\sqrt{\\tau}} \\]

\\[ d_2 = d_1 - \\sigma \\sqrt{\\tau} = \\frac{\\ln \\left(\\frac{S}{K}\\right) + \\left(r - \\frac{\\sigma^2}{2}\\right) \\tau}{\\sigma \\sqrt{\\tau}} \\]

Here we can remind ourself of the equation:

\\[d\\ln(S_t) = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) dt + \\sigma dB_t \\]

and remind \\( \\tau = T - t \\)

So, if we integrate t to T (or in \\(\\tau = T-t \\) to 0),

\\[ \\int_t^{T} d\\ln(S_u) = \\ln(S_T) - \\ln(S_t) = \\int_t^{T} \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) du + \\sigma \\int_t^{T} dB_u \\]

\\[ \\ln(S_T) - \\ln(S_t) = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) \\tau + \\sigma B_\\tau \\]

\\[ \\frac{\\ln\\left(\\frac{S_T}{S_t}\\right) - (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} =  \\frac{W_{\\tau}}{\\sqrt{\\tau}} = Z\\]

Let's define a random variable \\( X\\)

\\[X = \\ln\\left(\\frac{S_T}{S_t}\\right) \\]

As shown before, \\( X = (r - \\frac{1}{2} \\sigma^2) \\tau + \\sigma W_\\tau\\)

and \\( Z = \\frac{X - (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} \\)

Alternatively, we could indeed see what the expectation and variance of our X is:

\\[ X = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) \\tau + \\sigma B_\\tau \\]

Because \\( E(B_{\\tau}) = 0\\),

\\[ E[X] = E\\left[ \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) \\tau + \\sigma B_\\tau \\right] = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) \\tau\\]

Because, with fixed \\( \\tau \\), \\( ( \\mu - \\frac{1}{2} \\sigma^2 )\\) is a constant term:

\\[ \\text{Var}(X) = \\text{Var}\\left[ \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) \\tau + \\sigma B_\\tau \\right] = \\sigma^2 \\tau \\]

Now we can see \\( d_{2} \\) is a point evaluated at \\( K \\),

\\[ d_{2} = \\frac{\\ln\\left(\\frac{S_t}{K}\\right) + (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}}\\]

\\[ d_{2} = - (\\frac{\\ln\\left(\\frac{K}{S_{t}}\\right) - (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}})\\]

If we think of \\( d_{2}\\) in terms of X

\\[ X_{K} = \\ln\\left(\\frac{K}{S_t}\\right)\\]

Then

\\[ d_{2} = - \\frac{X_K - (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} \\]

By symmetry of the standard normal distribution,

\\[ P(Z \\leq -d_2) = P(Z \\geq d_2)\\]

From there, we get

\\[ P(Z \\le -d_2) = P(X \\leq -X_K) = P(X \\geq X_K) = P( S_{T} &gt; K )\\]

So 2nd term, \\( Ke^{-r(T-t)}N(d_2) \\) represents the expected excercising price as present value.

Now, let's handle \\( d_{1} \\),

\\[ d_1 = d_2 + \\sigma \\sqrt{\\tau} \\]

\\[ d_1 = - \\frac{X_K - (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} + \\sigma \\sqrt{\\tau} \\]
\\[ d_1 = - \\frac{X_K - (r + \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} \\]

Now,

\\[ \\ln(S_T) - \\ln(S_t) = \\left( \\mu - \\frac{1}{2} \\sigma^2 \\right) \\tau + \\sigma B_\\tau \\]

\\[ \\ln(S_T) - \\ln(S_t) + \\sigma^{2} \\tau = \\left( \\mu + \\frac{1}{2} \\sigma^2 \\right) \\tau + \\sigma B_\\tau \\]

\\[ \\frac{\\ln\\left(\\frac{S_T}{S_t}\\right) - (r - \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} =  \\frac{W_{\\tau}}{\\sqrt{\\tau}} = Z\\]

becomes

\\[ \\frac{\\ln\\left(\\frac{S_T}{S_t}\\right) + \\sigma^{2} \\tau - (r + \\frac{1}{2} \\sigma^2) \\tau}{\\sigma \\sqrt{\\tau}} =  \\frac{W_{\\tau}}{\\sqrt{\\tau}} = Z\\]

So,

\\[ Y = \\ln\\left(\\frac{S_T}{S_t}\\right) + \\sigma^{2} \\tau \\]

So Y is shifted version of X by \\( \\sigma^{2} \\tau \\)

If i try to guess.. (it is still not so clear)

In Bm, where change in X is linear to variance t.
Likewise, in GBM, X 's change is linear to variance \\( \\sigma^2 t\\),

and
\\[Y = X + \\sigma^2 \\tau = \\ln(S_{T}/S_{t}) + \\sigma^2 \\tau \\]
is effectively shifting the random variable as if we are looking at X after time &tau;.

So we are changing the perspective as if our variable has gained the variability over time, then we look at the probability of our random variable to be greater than a certain value.

Since, gaining variability flattens the distribution, probability of \\( X &gt; x_{1} \\) gets larger, or you could see \\( d_1 = d_2 + \\sigma \\sqrt{\\tau} \\) that \\( d_1 &gt; d_2 \\) so cdf with a larger value gets larger.

I expect this makes \\( N(d1) &gt; N(d2) \\).

But I can't see clearly why this shifting makes sense.
And the fact that we are not discounting makes that the time shift is happening so that our probability can be interpreted as an probability accessed in present time.


### Unverified interpretation {#unverified-interpretation}

The following is not verified but most likely true:

\\( N(d_{2}​) \\) represents the risk-neutral probability that the option will expire in-the-money (without adjusting for the volatility).

\\( N(d_{1}​)\\) accounts for volatility, which represents the probability of exercise adjusted for expected growth due to the stock's return distribution.

\\[\\Delta = \\frac{\\partial C}{\\partial S} = N(d_1) + S_t \\frac{\\partial N(d_1)}{\\partial S} - Ke^{-r\\tau} \\frac{\\partial N(d_2)}{\\partial S} \\]

After cancelling, we get
\\[ \\Delta = N(d_{1}) \\]


## Plotting the formula {#plotting-the-formula}

To plot the Black-Scholes formula for the price of a European call option, \\( C(t, S) \\), you'll need the following information:

1.  ****Stock Price, \\( S \\)****: The current price of the underlying stock.

2.  ****Strike Price, \\( K \\)****: The predetermined price at which the holder of the option can buy the stock if they decide to exercise the option.

3.  ****Time to Maturity, \\( \\tau = T - t \\)****: The time left until the option expires.

4.  ****Risk-Free Rate, \\( r \\)****: The interest rate for a risk-free investment, typically a short-term government bond rate.

5.  ****Volatility, \\( \\sigma \\)****: This represents the stock price's expected future volatility. It's the standard deviation of the stock's returns over a given period.

6.  ****Cumulative Distribution Function of the Standard Normal Distribution, \\( N(\\cdot) \\)****: This gives the probability that a normally distributed random variable will be less than a given value. In the context of the Black-Scholes formula, \\( d_1 \\) and \\( d_2 \\) are:

\\[ d_1 = \\frac{\\ln \\left(\\frac{S}{K}\\right) + \\left(r + \\frac{\\sigma^2}{2}\\right) \\tau}{\\sigma \\sqrt{\\tau}} \\]

\\[ d_2 = d_1 - \\sigma \\sqrt{\\tau} = \\frac{\\ln \\left(\\frac{S}{K}\\right) + \\left(r - \\frac{\\sigma^2}{2}\\right) \\tau}{\\sigma \\sqrt{\\tau}} \\]

Once you have all the required parameters and the above equations, you can compute \\( C(t, S) \\) for different values of \\( S \\) (stock price) and plot it. Typically, the x-axis represents the stock price \\( S \\) and the y-axis represents the option price \\( C(t, S) \\). This will give you a curve showing how the call option price changes as the underlying stock price changes.

Remember, the Black-Scholes formula assumes European options (can only be exercised at expiry), no dividends during the life of the option, and constant volatility and interest rates. If these assumptions don't hold, the actual option price may differ from the Black-Scholes price.

You can also plot the evolution of the option price \\( C(t, S) \\) over time, i.e., as the option approaches its maturity date. To do this, you'll keep the stock price \\( S \\) fixed and vary \\( \\tau = T - t \\) (time to maturity).

1.  ****Fixed Stock Price, \\( S \\)****: Choose a particular value for the stock price to see how the option value changes over time for that specific stock price.

2.  ****Vary Time to Maturity, \\( \\tau = T - t \\)****: Start with a value of \\( \\tau \\) close to the actual maturity (for example, \\( T \\)) and decrement it to approach zero. This will show the option price from the start of the option's life until its expiry.

3.  ****All other parameters****: Keep all other parameters like strike price \\( K \\), risk-free rate \\( r \\), and volatility \\( \\sigma \\) constant.

With these settings, you can plot \\( \\tau \\) (time to maturity) on the x-axis and \\( C(t, S) \\) on the y-axis. This will give you a curve showing how the call option price changes as time progresses and the option approaches its expiration.

A typical behavior you'll observe:

-   ****European Call Options without Dividends****: As expiration approaches, the option price tends to converge towards its intrinsic value, which is \\( max(S-K, 0) \\). If the option is in-the-money (i.e., \\( S &gt; K \\)), its value will be positive, and if it's out-of-the-money (i.e., \\( S &lt; K \\)), its value will approach zero.

-   ****European Put Options without Dividends****: Similarly, as expiration approaches, the put option price will converge to its intrinsic value, which is \\( max(K-S, 0) \\).

This graphical representation provides insights into the time decay (theta decay) of options, where the value of an option erodes as it gets closer to its expiration date, everything else being constant.


## Sample plotting {#sample-plotting}

We generate random stock price, and plot option price along with the stock price

\\[ d_1 = \\frac{\\ln(\\frac{S}{K}) + (r + \\frac{\\sigma^2}{2})t}{\\sigma\\sqrt{t}} \\]
\\[ d_2 = d_1 - \\sigma\\sqrt{t} \\]
\\[ C = S \\times N(d_1) - K \\times e^{-rt} \\times N(d_2) \\]
\\[ P = K \\times e^{-rt} \\times N(-d_2) - S \\times N(-d_1) \\]

```python
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy.stats import norm

# Black-Scholes Call Option formula

def black_scholes_call(S, K, T, r, sigma):
    if T <= 1e-5:  # A small threshold to handle near-zero time to maturity
        return max(0, S - K)
    d1 = (np.log(S/K) + (r + 0.5*sigma**2)*T) / (sigma*np.sqrt(T))
    d2 = d1 - sigma*np.sqrt(T)

    return S*norm.cdf(d1) - K*np.exp(-r*T)*norm.cdf(d2)

def black_scholes_put(S, K, T, r, sigma):
    if T <= 1e-5:  # A small threshold to handle near-zero time to maturity
        return max(0, K - S)

    d1 = (np.log(S/K) + (r + 0.5*sigma**2)*T) / (sigma*np.sqrt(T))
    d2 = d1 - sigma*np.sqrt(T)

    return K * np.exp(-r*T)*norm.cdf(-d2) - S * norm.cdf(-d1)

# Geometric Brownian Motion for S(t)
def GBM(S0, r, sigma, T, dt):
    t = np.arange(0, T+dt, dt)
    W = np.random.standard_normal(size = len(t))
    W = np.cumsum(W)*np.sqrt(dt)  # standard brownian motion
    S = S0*np.exp((r-0.5*sigma**2)*t + sigma*W)
    return S, t

# Parameters
S0 = 100          # initial stock price
K = 100           # strike price
r = 0.05          # risk-free rate
sigma = 0.2       # volatility
T = 1             # time to maturity in years
dt = 0.01         # time increment

# Simulate stock price path
S, t = GBM(S0, r, sigma, T, dt)

# Calculate call option prices for each time point
C = [black_scholes_call(s, K, T-ti, r, sigma) for s, ti in zip(S, t)]
P = [black_scholes_put(s, K, T-ti, r, sigma) for s, ti in zip(S, t)]
# Plotting
fig, ax1 = plt.subplots(figsize=(20,10))


ax1.axhline(y=K, color='gray', linestyle='--', label='Strike Price')
ax1.legend(loc='upper left')

color = 'tab:red'
ax1.set_xlabel('Time to Maturity (Years)')
ax1.set_ylabel('Stock Price', color=color)
ax1.plot(t, S, color=color)
ax1.tick_params(axis='y', labelcolor=color)

ax2 = ax1.twinx()  # instantiate a second axes that shares the same x-axis
color = 'tab:blue'
ax2.set_ylabel('Call Option Price', color=color)
ax2.plot(t, C, color=color)
ax2.tick_params(axis='y', labelcolor=color)


ax3 = ax1.twinx()
ax3.spines["right"].set_position(("axes", 1.1))
ax3.spines["right"].set_visible(True)

color = 'tab:green'
ax3.set_ylabel('Put Option Price', color=color)
ax3.plot(t, P, color=color)
ax3.tick_params(axis='y', labelcolor=color)


plt.title('Stock Price and Call Option Price Over Time')
plt.grid(True)
plt.show()
```

{{< figure src="/ox-hugo/2023-10-21-stock_option.png" >}}

```python
from scipy.optimize import newton, fsolve

def vega(S, K, T, r, sigma):
    d1 = (np.log(S / K) + (r + 0.5 * sigma**2) * T) / (sigma * np.sqrt(T))
    vega = S * norm.pdf(d1) * np.sqrt(T)
    return vega

def option_price_difference(sigma, *args):
    market_price, S, K, T, r = args
    return black_scholes_call(S, K, T, r, sigma) - market_price

def newton_iterations(func, x0, fprime, args):
    iterations = [0]  # Use a list so it can be modified inside the function

    def func_with_count(x, *args):
        iterations[0] += 1
        return func(x, *args)

    newton(func_with_count, x0, fprime=fprime, args=args)
    return iterations[0]

# Wrapper for fsolve to count iterations
def fsolve_iterations(func, x0, args):
    iterations = [0]  # Use a list so it can be modified inside the function

    def func_with_count(x, *args):
        iterations[0] += 1
        return func(x, *args)

    fsolve(func_with_count, x0, args=args)
    return iterations[0]

market_price = K
initial_volatilities = np.linspace(0.1, 0.5, 10)
for x0 in initial_volatilities:
    newton_iters = newton_iterations(option_price_difference, x0, vega, args=(market_price, S, K, T, r))
    fsolve_iters = fsolve_iterations(option_price_difference, x0, args=(market_price, S, K, T, r))
    print(f"Initial guess: {x0:.2f}, Newton iterations: {newton_iters}, fsolve iterations: {fsolve_iters}")
```


### reading the plot {#reading-the-plot}

The call option price, as described by the Black-Scholes formula, will exhibit a certain sensitivity to the underlying stock price. This sensitivity is quantified by the option's delta (\\(\\Delta\\)), which, as we discussed earlier, is the derivative of the option price with respect to the stock price: \\(\\Delta = \\frac{\\partial C}{\\partial S}\\).

A few points to note:

1.  ****In the Money vs. Out of the Money****: If the stock price is significantly above the strike price (meaning the option is deep "in the money"), the call option's price will tend to move almost one-for-one with the stock price. Conversely, if the stock price is significantly below the strike price (option is "out of the money"), the call option's price may exhibit much less sensitivity to changes in the stock price.

2.  ****Time to Expiry****: As the expiration date of the option approaches, the option's sensitivity to changes in the stock price may increase, especially if the option is near the money (stock price close to the strike price). This is because there is less time for the stock to make significant moves, making the option more sensitive to any change in the stock price.

3.  ****Volatility****: Higher volatility increases the likelihood of the option ending in the money, which can increase the option's price even if the stock price remains unchanged. Conversely, a decrease in volatility can reduce the option's price.

4.  ****Option Premium vs. Stock Price****: Remember that while the stock price can theoretically range from zero to infinity, the option price is bounded. A call option's price can never exceed the stock price (since you wouldn't pay more for an option than just buying the stock outright), and it will never go below zero.

5.  ****Other Factors****: Interest rates (through the discounting factor) and dividends (not considered in our simple model) can also influence the option price.

In the plots, you'll observe that the option price doesn't mirror the stock price perfectly, but it does follow its general movements, reflecting the combination of these factors. The key insight is that option pricing is a balance between the intrinsic value (the immediate value if exercised) and the time value (the value from the potential for the stock price to move before expiration).


## Controlled movement {#controlled-movement}

We see the option price change as time changes (with stock price fixed)

```python
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.stats import norm

# Define the Black-Scholes Call Option formula
def black_scholes_call(S, K, T, r, sigma):
    if T <= 1e-5:
        return max(0, S - K)
    d1 = (np.log(S/K) + (r + 0.5*sigma**2)*T) / (sigma*np.sqrt(T))
    d2 = d1 - sigma*np.sqrt(T)
    return S*norm.cdf(d1) - K*np.exp(-r*T)*norm.cdf(d2)

# Parameters
K = 100
r = 0.05
sigma = 0.2

time_to_maturity = np.linspace(0.01, 1, 100)
stock_prices = np.linspace(50, 150, 100)

# Plot 1: Option price vs. Time-to-maturity (fixed stock price)
fixed_S = 100
option_prices_t = [black_scholes_call(fixed_S, K, T, r, sigma) for T in time_to_maturity]

plt.figure(figsize=(10, 6))
plt.plot(time_to_maturity, option_prices_t)
plt.title(f'Option Price vs Time-to-maturity (S = {fixed_S})')
plt.xlabel('Time to Maturity')
plt.ylabel('Option Price')
plt.grid(True)
plt.show()

# Plot 2: Option price vs. Stock price (fixed time-to-maturity)
fixed_T = 0.5
option_prices_S = [black_scholes_call(S, K, fixed_T, r, sigma) for S in stock_prices]

plt.figure(figsize=(10, 6))
plt.plot(stock_prices, option_prices_S)
plt.title(f'Option Price vs Stock Price (T-t = {fixed_T})')
plt.xlabel('Stock Price')
plt.ylabel('Option Price')
plt.grid(True)
plt.show()

# Plot 3: Heatmap of option price as function of both time and stock price
option_prices = np.zeros((100, 100))
for i, T in enumerate(time_to_maturity):
    for j, S in enumerate(stock_prices):
        option_prices[i, j] = black_scholes_call(S, K, T, r, sigma)

plt.figure(figsize=(10, 8))
sns.heatmap(option_prices, cmap="YlGnBu", cbar_kws={'label': 'Option Price'})
plt.title('Black-Scholes Call Option Price')
plt.xlabel('Stock Price')
plt.ylabel('Time to Maturity')
plt.xticks(ticks=np.arange(0, 100, 10), labels=np.round(stock_prices[::10], 2))
plt.yticks(ticks=np.arange(0, 100, 10), labels=np.round(time_to_maturity[::10], 2))
plt.show()

```
