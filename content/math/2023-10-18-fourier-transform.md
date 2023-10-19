+++
title = "Fourier transform"
author = ["littlehome"]
date = 2023-10-18
lastmod = 2023-10-19T16:00:51+09:00
draft = false
+++

## Fourier transform (part2) {#fourier-transform--part2}

This is part2 after [fourier series]({{< relref "2023-10-15-fourier_series#fourier-series" >}})

This is summary of lecture 5-7 of <https://www.youtube.com/playlist?list=PLB24BC7956EE040CD>

The Gaussian fourier transform is discussed more in the chat.
<https://chat.openai.com/share/bc7157eb-da88-447d-ab6c-422c7bef80f2>


## Fourier Transform and the Heat Equation {#fourier-transform-and-the-heat-equation}


### Heat Equation for a Heated Ring {#heat-equation-for-a-heated-ring}

Consider a ring that is initially heated in a certain manner. We can describe the temperature distribution across the ring as a function of position \\(x\\) and time \\(t\\).

-   Initial temperature distribution: \\( f(x) \\)
-   Temperature at a position \\(x\\) at time \\(t\\): \\( u(x, t) \\)

    Due to the symmetry of the ring, the temperature distribution is periodic in \\(x\\) with period 1 (for simplicity). Therefore, we can express the periodicity conditions as:
    \\[ f(x + 1) = f(x) \\]
    \\[ u(x + 1, t) = u(x, t) \\]

    This periodicity arises from the symmetric nature of the object. As time progresses, the temperature distribution will evolve, and by using the Fourier transform, we can study the dynamics of \\( u(x, t) \\).


### Further Steps {#further-steps}

To fully exploit the Fourier transform in this context, we'd typically proceed by:

1.  Expressing \\( f(x) \\) in terms of its Fourier series.
2.  Applying the heat equation to each term in the series.
3.  Summing up the results to get the temperature distribution \\( u(x, t) \\) for any given time \\( t \\).

    With this approach, the Fourier transform provides an elegant solution to the heat equation for a periodically heated object like our ring.


### Formulation {#formulation}

The solution for \\( u(x, t) \\) in terms of its Fourier components is:
\\[ u(x,t) = \sum\_k C\_k(t) e^{2 \pi i k x} \\]

The heat equation is given by:
\\[ U\_t = \frac{1}{2} U\_{xx} \\]


### Coefficient Dynamics {#coefficient-dynamics}

On substituting the expression for \\( u(x, t) \\) into the heat equation and equating like terms, the time evolution of the coefficients \\( C\_k(t) \\) is given by:
\\[ \dot{C\_k}(t) = -2 \pi^2 k^2 C\_k(t) \\]
Which has the solution:
\\[ C\_k(t) = C\_k(0) e^{-2 \pi^2 k^2 t} \\]


### Initial Coefficients {#initial-coefficients}

To obtain \\( C\_k(0) \\), one must expand the initial condition \\( f(x) \\) in its Fourier series and identify the coefficients.


### Initial Condition and Fourier Coefficients {#initial-condition-and-fourier-coefficients}

Given the initial temperature distribution \\( u(x, 0) \\), we can express it as:
\\[ u(x, 0) = f(x) = \sum\_k C\_k(0) e^{2\pi i k x} \\]

The \\( k \\)-th Fourier coefficient of \\( f(x) \\) is given by:
\\[ C\_k(0) = \int\_0^1 f(x) e^{-2\pi i k x} \\, dx \\]

By calculating \\( C\_k(0) \\) for all values of \\( k \\), we get a complete representation of the initial temperature distribution in terms of its Fourier components.


## Understanding the Heat Equation and Its Implications {#understanding-the-heat-equation-and-its-implications}


### What Have We Achieved? {#what-have-we-achieved}

We started with the heat equation, a partial differential equation, and then used Fourier techniques to find a closed form solution for \\( u(x,t) \\).


### Cooling Over Time {#cooling-over-time}

One immediate insight from our closed form solution is that as \\( t \to \infty \\), \\( u(x,t) \to 0 \\). In plain terms? Our ring cools off over time, approaching a uniform temperature.


#### Conservation of Energy {#conservation-of-energy}

At its core, the heat equation reflects the conservation of energy. Energy isn't magically appearing or disappearing; it's merely spreading out. But without a constant source of heat, this spreading leads to an overall decrease in perceived temperature.


### Periodicity in Space: A Circular Flow? {#periodicity-in-space-a-circular-flow}

Since our problem deals with a 1D heat equation and we've assumed periodicity in \\( x \\), we're talking about a circle, with heat flowing in a circular manner.


#### Thinking in Circles {#thinking-in-circles}

Given the setup, you can think of the "1D" aspect as a straight line bent into a circle (like a ring). The periodicity in \\( x \\) essentially captures this circular nature. So, heat isn't just moving left or right; it's circulating around the ring.


### but if we are considering heat flowing circle, it should be preserved, why is it cooling off? {#but-if-we-are-considering-heat-flowing-circle-it-should-be-preserved-why-is-it-cooling-off}

I haven't got answers for this


## Transition from Fourier Series to Fourier Transform {#transition-from-fourier-series-to-fourier-transform}

Suppose we have a function which looks like the following.

{{< figure src="/ox-hugo/rectangle_plot.png" >}}

The graph is not periodic, and we still want to express it with sum of signals.
Suppose, the domain of the function is (a, b).
We are going to pick a large enough T such that (\\(\frac{-1}{2} T, \frac{1}{2} T)\\) would cover the domain (a, b).
And we want to make T go to infinity to cover any (non-periodic) function of any domain.


### Fourier Series: Describing Periodic Phenomena {#fourier-series-describing-periodic-phenomena}

The Fourier series provides a way to represent periodic functions as a sum of sines and cosines, which can be equivalently represented in terms of complex exponentials.

-   Formula: \\( f(t) = \sum\_{k} C\_k e^{\frac{2\pi i k t}{T}} \\)
-   Here, \\( f(t) \\) is periodic with period \\( T \\).


### Transition to Non-periodic Functions {#transition-to-non-periodic-functions}

The idea is to view non-periodic functions as the limiting case of periodic functions as their period goes to infinity.

-   As \\( T \rightarrow \infty \\), the spacing between frequency components (given by \\( \frac{1}{T} \\)) shrinks towards zero.
-   This leads us from a discrete spectrum (as in Fourier series) to a continuous spectrum, reflecting the non-periodic nature of the function.


### Fourier Transform: Generalization for Non-periodic Functions {#fourier-transform-generalization-for-non-periodic-functions}

By taking this limit, we move from the discrete Fourier coefficients of the series to the continuous Fourier Transform.


## Detailed Transition from Fourier Series to Fourier Transform {#detailed-transition-from-fourier-series-to-fourier-transform}


### Challenge with Naive Approach {#challenge-with-naive-approach}

Directly letting \\( T \rightarrow \infty \\) in the Fourier series coefficients \\( C\_k \\) causes them to diminish. Specifically:

-   \\( C\_k = \frac{1}{T} \int f(t) e^{-\frac{2\pi i k t}{T}} dt \\)
-   As \\( T \rightarrow \infty \\), \\( C\_k \\) approaches 0 when area of the function is bounded since it becomes \\( \frac{1}{T} \\) times the area (essentially an average over an increasingly large interval).


### Introducing an Intermediate Function {#introducing-an-intermediate-function}

To overcome this issue, we introduce an auxiliary function:

\begin{aligned}
g\_{f}\left(\frac{k}{T}\right) = \int f(t) e^{-2\pi i \frac{k}{T} t} dt  \\\\
\end{aligned}

Then the series become:

\\[ f(t) = \sum\_{k} g\_{f}\left(\frac{k}{T}\right) e^{2\pi i \frac{k}{T} t} \frac{1}{T} \\]


### Transitioning to Continuous Spectrum {#transitioning-to-continuous-spectrum}

As \\( T \rightarrow \infty \\), the discrete frequency variable \\( \frac{k}{T} \\) transitions to a continuous variable \\( s \\).
The factor \\( \frac{1}{T} \\) in the sum of the Fourier series play the role of a differential element \\( ds \\) in the integral.

The coefficent becomes:
\\[ g\_{f}(s) = \int  e^{-2\pi i s t} f(t) dt \\]

And the series become:
\\[ f(t) = \int g\_{f}(s) e^{2\pi i s t} ds \\]


## Example, FT of rectangle function {#example-ft-of-rectangle-function}

We look at the simplist example of Fourier transform.

{{< figure src="/ox-hugo/rectangle_plot.png" >}}

Given the rectangle signal, we can apply the fourier transform by applying the formula.

\\[ g\_{f}(s) = \int\_{\frac{-1}{2}}^{\frac{1}{2}} e^{-2\pi i s t} dt = \frac{sin(\pi s)}{\pi s}\\]

{{< figure src="/ox-hugo/sinc_plot_seaborn.png" >}}

Sinc function shows that we need many (infinitely many) sinusoidal functions at differernt frequencies to construct the rect function. (This is due to the discontinuity (sharp edge) of the rectangle at both ends.)


## Dual Representation {#dual-representation}

-   Every signal has a spectrum. The spectrum determines the signal
-   FT provides two representation for single phenomena.


## Guassian's Fourier transform is itself {#guassian-s-fourier-transform-is-itself}

\\[ f(t) = e^{-\pi t^{2}}\\]

\\[ g\_{f}(s) = e^{-\pi s^{2}}\\]

It's rather remarkable.

I can view gaussian arising as sum of IID random variables (CLT)

Or I can view it as blueprint where an architect built the system with sinusoidal functions where the weight of each sinusoidal function's frequency is precisely equal to the weight (probability) of phenomena observed.

Or One can view it as someone (the gaussian) who is capable of describing himself as observables (the gaussian distribution, observable domain) or as weight of the signals that will create the observables (spectrum domain).
And it is indistinguishable which domain he is showing himself in.

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
num_samples = 1000
x = np.linspace(-10, 10, num_samples)
gaussian = np.exp(-x**2)

# Define a range of frequencies
frequencies = np.linspace(-10, 10, num_samples)

# Initialize an array to store our sum of sinusoids
reconstructed_signal = np.zeros_like(x)

# Iterate over frequencies and sum up sinusoids using weights from Gaussian
for i, freq in enumerate(frequencies):
    weight = np.exp(-freq**2)  # This is our Fourier-transformed Gaussian
    sinusoid = weight * np.cos(2 * np.pi * freq * x)  # Using cosine now
    reconstructed_signal += sinusoid

# Normalize the result
reconstructed_signal /= num_samples

# Plot
plt.figure(figsize=(10, 4))

plt.subplot(1, 2, 1)
plt.plot(x, gaussian, label="Original Gaussian")
plt.legend()

plt.subplot(1, 2, 2)
plt.plot(x, reconstructed_signal, label="Reconstructed from Sinusoids", alpha=0.7)
plt.legend()

plt.tight_layout()
plt.show()

```

{{< figure src="/ox-hugo/gaussian.png" >}}


## prerequisite math {#prerequisite-math}


### Euler's formula {#euler-s-formula}

What does it mean when we have \\( e^i \\) ?

<https://chat.openai.com/share/24a3ebdf-272d-487d-9310-669d6dd5fc11>


### CLT {#clt}

CLT can be proved with fourier transorm

<https://chat.openai.com/share/d0eb26b0-8ca9-4cb1-a5d8-a29d38380cb4>
