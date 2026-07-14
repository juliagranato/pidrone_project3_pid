# Project 3 PID Answers

## Part 1: Altitude PID in Simulation

### Problem 1
  1. 1434
  2. For large values of $K_p$ such as 50, 500, and 5000, the drone experiences large oscillations that span approximately one meter, which make it too unstable to fly. When $K_p$ is 5000, the oscillations experience a pattern of different peak heights.
  3. When the $K_p$ term is zero, the drone stays on the ground for all values of $K_d$ including 50, 500, 5000. This makes sense because without additional thrust from the P term to get the drone off the ground, the error does not change between time steps (as the drone sits on the ground) and the D term has no effect.
  4. Increasing the $K_p$ to $K_d$ ratio decreases rise time, but increases overshoot. With a high $K_p$ to $K_d$ ratio, the system has a very aggressive response and may sustain additional oscillations before settling. If the $K_p$ to $K_d$ ratio is too low, the system is very sluggish and will take a long time to reach the set point, potentially without any overshoot.
  5. The I term reduces steady state error and allows the drone to hover at the desired setpoint by factoring in the error contributed by outside sources including gravity. When $K_p$ and $K_d$ are set to zero, but $K_i$ is nonzero, the system experiences massive sustained oscillations and is incredibly unstable.
  6.
  7.  $K_p$:  
      $K_i$:  
      $K_d$:  

### Problem 2
  1.  $K_p$:  
      $K_i$:  
      $K_d$:  
  2.
  3.

### Problem 3
  1.  $K_p$:  
      $K_i$:  
      $K_d$:  
  2.  

## Part 2: Tuning

### Problem 1
  1.  
  2.  

### Problem 2
  1.
