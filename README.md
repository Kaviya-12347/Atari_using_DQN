📘 Atari DQN — Deep Q-Network Agent (PyTorch)

This repository contains a clean and modular implementation of a Deep Q-Network (DQN) agent that learns to play Atari games directly from pixel input. The project follows the classic DQN approach introduced by DeepMind (Mnih et al., 2015) and includes essential RL components such as experience replay, target networks, and epsilon-greedy exploration.

<p align="center"> <img src="https://upload.wikimedia.org/wikipedia/en/5/5f/Breakout_arcade_gameplay.png" width="450"/> </p>

🚀 Project Overview

This project implements a reinforcement learning agent that learns to play BreakoutNoFrameskip-v4 using raw Atari frames. The agent observes stacks of preprocessed frames, feeds them through a convolutional neural network, and uses Q-learning to maximize expected rewards.

The implementation is fully modular and organized for easy extension (e.g., Double DQN, Dueling Networks, Prioritized Replay).

🎯 Key Features

✔️ CNN-based DQN architecture (Nature DQN)

✔️ Experience Replay Buffer for stabilizing training

✔️ Target Network to reduce Q-value oscillation

✔️ Atari preprocessing (frame skipping, grayscale, resizing, frame stacking)

✔️ ε-Greedy Exploration with linear decay

✔️ Clean and modular code structure

✔️ TensorBoard logging for reward/loss monitoring

✔️ Model checkpointing every N frames

🧠 DQN Architecture
Input: 4 stacked grayscale frames (84x84)

Convolutional Neural Network:
────────────────────────────────────────
Conv1: 32 filters, 8×8 kernel, stride 4 → ReLU  
Conv2: 64 filters, 4×4 kernel, stride 2 → ReLU  
Conv3: 64 filters, 3×3 kernel, stride 1 → ReLU  
Flatten  
FC1: 512 units → ReLU  
FC2: #actions → Q-values
────────────────────────────────────────
Output: Q-values for each action


📊 Logging & Visualization

Training logs are saved using TensorBoard:

tensorboard --logdir runs/

You can visualize:

Episodic rewards

Loss curves

Epsilon decay

Frame progression

🏆 Results (Expected)

With enough training (1M–5M frames), a vanilla DQN agent typically learns:

Paddle tracking

Ball interception

Basic survival and scoring strategies

Performance improves steadily as episodic rewards increase.
