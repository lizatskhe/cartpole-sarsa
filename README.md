# CartPole - SARSA Algo

The CartPole is a classic reinforcement learning benchmark where the goal is to balance a pole upright on a moving cart. The agent can apply a force to move the cart left or right, and must learn to keep the pole from falling over for as long as possible.

The environment provides a continuous state space consisting of:

- Cart position

- Cart velocity

- Pole angle

- Pole angular velocity

The task ends if the pole falls too far or the cart moves out of bounds. The agent receives a reward of +1 for every timestep it keeps the pole balanced.

![cartpole](https://github.com/user-attachments/assets/3ec619b0-5f8e-4143-b95d-dd3a5b82faeb)

## SARSA Algorithm

**Discrete State Representation:**
The continuous observation space is discretized into bins for compatibility with tabular SARSA.

**SARSA Algorithm:**
The agent learns an on-policy value function using the SARSA update rule.

**Exploration vs. Exploitation:**
Uses an epsilon-greedy strategy with exponential decay to balance exploration and exploitation.

**Training Setup:**

- Bins: 20 per dimension

- Episodes: 20,000

- Learning rate (α): 0.05

- Discount factor (γ): 0.995

- Initial epsilon: 1.0 (decays to 0.01)

**Performance Evaluation:**

- Average rewards are logged every 500 episodes.

- Policy is evaluated (with greedy action selection) and visualized every 10,000 episodes.

- Evaluation videos are recorded and merged into a final output.

  ![average_rewards](https://github.com/user-attachments/assets/4a8ab3d7-b769-4fe9-8dde-092e5a57ec20)

  ![max_q_value](https://github.com/user-attachments/assets/343149f7-f4db-4049-ae5f-f0f9ebb3fc9b)



