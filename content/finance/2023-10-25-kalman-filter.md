+++
title = "Kalman Filter"
author = ["littlehome"]
date = 2023-10-26
lastmod = 2023-10-30T15:48:38+09:00
draft = false
+++

## Resources {#resources}

<https://youtu.be/-DiZGpAh7T4?si=YN-a_mZ1gdwlt54n>

<https://web.mit.edu/kirtley/kirtley/binlustuff/literature/control/Kalman%20filter.pdf>

<https://arxiv.org/pdf/1910.03558.pdf>

<https://chat.openai.com/share/d2e080cf-607c-4492-a359-f43c4e7e3daa> (gpt)


## Kalman filter {#kalman-filter}

The Kalman filter operates in a loop with the main stages being prediction and update.

It has model (state) which drives the pheonomenon (observation)
The transition from prev state to next state is linear.
The state to observation is linear.

With updated observation, you update your model so that your prediction is getting better by balancing the weight of 'model prediction' and 'current observation'.

For instance, where you are moving linearly, kalman filter tries to construct a model (parameters) to describe observation better on each observation.

1.  ****Initialization****:
    -   Start with an initial estimate of the state, \\( x\_0 \\).
    -   Provide an initial estimate of the error covariance, \\( P\_0 \\).

2.  ****Prediction Phase****:
    -   ****State Prediction****: Using the system dynamics, predict the state at the next time step. This prediction uses the most recent state estimate.
        \\( x\_{k+1|k} = Ax\_{k|k} \\)
    -   ****Error Covariance Prediction****: Also predict the error covariance associated with this state prediction.
          \\( P\_{k+1|k} = AP\_{k|k}A^T + Q \\)
        where \\( Q \\) is the process noise covariance.

3.  ****Measurement Update (Correction) Phase****:
    -   ****Compute Kalman Gain****: This determines how much the prediction should be adjusted based on the new measurement. It's a balance between how much we trust our prediction vs. the measurement.
          \\( K\_{k+1} = P\_{k+1|k} H^T (HP\_{k+1|k} H^T + R)^{-1} \\)
        where \\( H \\) is the measurement model and \\( R \\) is the measurement noise covariance.
    -   ****State Estimate Update****: Correct the prediction with the measurement to get a refined state estimate.
          \\( x\_{k+1|k+1} = x\_{k+1|k} + K\_{k+1}(y\_{k+1} - Hx\_{k+1|k}) \\)
        where \\( y\_{k+1} \\) is the measurement at time \\( k+1 \\).
    -   ****Error Covariance Update****: Update the error covariance to reflect the new knowledge from the measurement.
        \\( P\_{k+1|k+1} = (I - K\_{k+1}H)P\_{k+1|k} \\)

4.  ****Loop****:
    -   Return to the Prediction Phase and repeat for the next time step.

Throughout this process, the Kalman filter effectively combines knowledge from:

-   The system's own dynamics (how it believes it evolves over time).
-   The new measurements (direct observations of the system).

By combining these two sources of information, the Kalman filter provides a statistically optimal estimate of the state of the system under the assumptions of the model.


### Derivation of Kalman gain {#derivation-of-kalman-gain}

The derivation of the Kalman gain can indeed be motivated by a similar logic as the one we followed earlier.

To derive the Kalman gain, we're essentially trying to minimize the posterior error (or the error after the update), given the new measurement. Like before, let's denote the estimation error after incorporating the measurement as:

\\[ e\_{k+1|k+1} = x\_{k+1} - x\_{k+1|k+1} \\]

With the Kalman update, the updated estimate is:

\\[ x\_{k+1|k+1} = x\_{k+1|k} + K\_{k+1}(y\_{k+1} - C x\_{k+1|k}) \\]

(So, in a sense, the above equation gives the meaning of the kalman gain. We are trying to find K for the above equation which will minimize the MSE)

Substituting in for our error:

\\[ e\_{k+1|k+1} = x\_{k+1} - x\_{k+1|k} - K\_{k+1}(y\_{k+1} - C x\_{k+1|k}) \\]

Now, using our system dynamics, we know:
\\[ y\_{k+1} = C x\_{k+1} + v\_{k+1} \\]
Where \\( v\_{k+1} \\) is our measurement noise.

Rearranging gives:
\\[ e\_{k+1|k+1} = (I - K\_{k+1} C) e\_{k+1|k} - K\_{k+1} v\_{k+1} \\]

To minimize the expected value of the squared error, we can consider its covariance matrix:

\\[ E[e\_{k+1|k+1} e\_{k+1|k+1}^T] \\]

Expanding this out and considering the cross term of the error and measurement noise, we get:
\\[ E[e\_{k+1|k} e\_{k+1|k}^T] - E[K\_{k+1} C e\_{k+1|k} e\_{k+1|k}^T] - E[e\_{k+1|k} e\_{k+1|k}^T C^T K\_{k+1}^T] + E[K\_{k+1} v\_{k+1} v\_{k+1}^T K\_{k+1}^T] \\]

We aim to minimize this expression by selecting the best \\( K\_{k+1} \\). Differentiating w.r.t \\( K\_{k+1} \\) and setting the result to zero (like we did previously), and recognizing the error covariance matrix \\( P\_{k+1|k} = E[e\_{k+1|k} e\_{k+1|k}^T] \\), we get:

\\[ K\_{k+1} = P\_{k+1|k} C^T (C P\_{k+1|k} C^T + R)^{-1} \\]

This is the Kalman gain. The process we followed mirrors the reasoning we used in the simpler estimation problem, but now in the context of state-space models and dynamical systems.


## Implementaion {#implementaion}

```python
import numpy as np
import matplotlib.pyplot as plt

np.random.seed(0)
```

```python
def get_volt():
    """Measure voltage."""
    v = np.random.normal(0, 2)   # v: measurement noise.
    volt_true = 14.4             # volt_true: True voltage [V].
    measured = volt_true + v  # z_volt_meas: Measured Voltage [V] (observable).
    return measured


def kalman_filter(measured, u_estimate, P):
    """Kalman Filter Algorithm for One Variable."""
    # (1) Prediction.
    # u_estimate is previous step's estimate
    # u_prediction is this step's prediction
    # P_prediction is covariance (?)

    u_prediction = A * u_estimate # prediction by last estimate (best guess)
    P_prediction = A * P * A + Q  # update uncertainties

    # (2) Kalman Gain.
    K = P_prediction * H / (H * P_prediction * H + R)

    # (3) Estimation.
    u_estimate = u_prediction + K * (measured - H * u_prediction)

    # (4) Error Covariance.
    P = P_prediction - K * H * P_prediction

    return u_estimate, P
```

```python
# Input parameters.
time_end = 10
dt = 0.2

# Initialization for system model.
A = 1
H = 1
Q = 0
R = 4
# Initialization for estimation.
x_0 = 12  # 14 for book.
P_0 = 6

time = np.arange(0, time_end, dt)
n_samples = len(time)
volt_measured_save = np.zeros(n_samples)
volt_esti_save = np.zeros(n_samples)
```

```python
u_estimate, P = None, None
for i in range(n_samples):
    measured = get_volt()
    if i == 0:
        u_estimate, P = x_0, P_0
    else:
        u_estimate, P = kalman_filter(measured, u_estimate, P)

    volt_measured_save[i] = measured
    volt_esti_save[i] = u_estimate
```

```python
plt.plot(time, volt_measured_save, 'r*--', label='Measurements')
plt.plot(time, volt_esti_save, 'bo-', label='Kalman Filter')
plt.legend(loc='upper left')
plt.title('Measurements v.s. Estimation (Kalman Filter)')
plt.xlabel('Time [sec]')
plt.ylabel('Voltage [V]')
# plt.savefig('png/simple_kalman_filter.png')
plt.show()
```

{{< figure src="/ox-hugo/2023-10-25-kalman.png" >}}
