# Project 3 PID Answers

## Part 1: Altitude PID in Simulation

### Problem 1
  1. 1434
  2. For large values of $K_p$ such as 50, 500, and 5000, the drone experiences large oscillations that span approximately one meter, which make it too unstable to fly. When $K_p$ is 5000, the oscillations experience a pattern of different peak heights.
  3. When the $K_p$ term is zero, the drone stays on the ground for all values of $K_d$ including 50, 500, 5000. This makes sense because without additional thrust from the P term to get the drone off the ground, the error does not change between time steps (as the drone sits on the ground) and the D term has no effect.
  4. Increasing the $K_p$ to $K_d$ ratio decreases rise time, but increases overshoot. With a high $K_p$ to $K_d$ ratio, the system has a very aggressive response and may sustain additional oscillations before settling. If the $K_p$ to $K_d$ ratio is too low, the system is very sluggish and will take a long time to reach the set point, potentially without any overshoot.
  5. The I term reduces steady state error and allows the drone to hover at the desired setpoint by factoring in the error contributed by outside sources including gravity. When $K_p$ and $K_d$ are set to zero, but $K_i$ is nonzero, the system experiences massive sustained oscillations and is incredibly unstable.
  6. If the reset method is not implemented correctly, the reset could cause integral windup.
  7.  $K_p$: 9.20 
      $K_i$: 0.20 
      $K_d$: 2.80

### Problem 2
  1.  $K_p$: 3.0
      $K_i$: 0.1
      $K_d$: 1.45
  2. The $K_p$, $K_i$, and $K_d$ terms are significantly lower (at least 50% of their previous value) when latency is factored into the model. 
  3. When the feedback is delayed, the proportional term reacts based on old data, so acting too aggressively can cause overshooting. It makes sense to lower $K_p$ so that the system takes more conservative actions while waiting for the process data to catch up. When there is latency, the controller is still receiving error after the system responds. This means that the integral term continues to accumulate error after the output has changed. This excessive accumulation of error leads to integral windup, so it makes sense to have a low $K_i$. The derivative term anticipates the future state by looking at how the rate of error changes. When there is latency, the controller is trying to anticipate a future state that has already occurred, which corrupts the prediction process and could potentially cause a chaotic and unstable response. It makes sense to lower $K_d$ to reduce these impacts.

### Problem 3
  1.  $K_p$: 3.0
      $K_i$: 0.08
      $K_d$: 1.30
  2. The addition of noise and drag causes small changes to the values of the PID constants When the sensors are very noisy the error difference between two time steps is a less accurate predictor of the next step, and it makes sense that the derivative term would be weighted less. 