# Robot Learning & ML Control

Five projects applying machine learning to robot navigation, manipulation, and control — implemented from scratch in Python/PyTorch as part of MECS6616 (Robot Learning) at Columbia University.

---

## Project Index

### 🏆 [Project 3 — Learned Dynamics MPC for a Multi-Link Robot Arm](./mecs6616_Spring2025_Project3_gc2905.ipynb)
**Approach:** Collected rollout data from a simulated multi-link arm, trained a neural network forward dynamics model, then embedded that learned model inside a Model Predictive Control (MPC) loop to reach goal configurations.

- Implemented MPC from scratch with a ground-truth dynamics model (Part 1)
- - Collected training data via MPC rollouts; trained a neural net forward model (Part 2)
  - - Replaced ground-truth dynamics with the learned model inside MPC — evaluated on 1-, 2-, and 3-link arm configurations (Part 3)
    - - Submitted: trained model checkpoints (`.pth`) + collected datasets (`.pkl`)
     
      - > **Why it matters:** Learning a forward dynamics model from data and using it for planning is the same systems-level approach BCI teams use for neural signal prediction and closed-loop control.
        >
        > ---
        >
        > ### 🏆 [Project 4 — Diffusion Policy & Generative BC for Push-T Manipulation](./mecs6616_Spring2025_Project4_gc2905.ipynb)
        > **Approach:** Implemented three behavioral cloning agents from scratch on the Push-T dexterous manipulation task, using receding-horizon control.
        >
        > - **Part I — Residual MLP:** Flattened observation history → action sequence prediction with MSE loss
        > - - **Part II — CVAE Agent:** Conditional VAE with encoder/decoder, KL divergence loss (β-weighted), reparameterization trick
        >   - - **Part III — Diffusion Policy (DDPM):** Implemented cosine noise schedule, forward/reverse diffusion, noise prediction network, and full denoising inference loop
        >    
        >     - > **Why it matters:** Implements DDPM and CVAE from scratch — directly relevant to generative approaches in foundation models and learned control policies.
        >       >
        >       > ---
        >       >
        >       > ### [Project 5 — Deep Q-Network (DQN) & PPO for Robot Arm Goal Reaching](./mecs6616_Spring2025_Project5_gc2905.ipynb)
        >       > **Approach:** Reinforcement learning applied to a robot arm reaching task using an OpenAI Gym-compatible environment.
        >       >
        >       > - **Part 1 — DQN from scratch:** Q-network, replay buffer, target network updates, ε-greedy exploration — no RL libraries
        >       > - - **Part 2 — PPO:** Used Stable-Baselines3 PPO on the same `ArmEnv` environment; trained with parallel environments for efficiency
        >       >  
        >       >   - > **Why it matters:** Building RL infrastructure from scratch (not just calling library APIs) demonstrates genuine understanding of the algorithms.
        >       >     >
        >       >     > ---
        >       >     >
        >       >     > ### [Project 2 — Neural Network Behavioral Cloning (2D Maze)](./mecs6616_Spring2025_Project2_gc2905.ipynb)
        >       >     > **Approach:** Extended Project 1 with deep neural networks (PyTorch). Three parts:
        >       >     > - MLP policy on low-dimensional (x,y) observations
        >       >     > - - CNN policy on 64×64 RGB images
        >       >     >   - - Multi-map generalization: model trained on multiple obstacle maps, tested on unseen configurations
        >       >     >    
        >       >     >     - ---
        >       >     >
        >       >     > ### [Project 1 — Classical ML for Robot Navigation (2D Maze)](./gc2905_Spring2025_Project1.ipynb)
        >       >     > **Approach:** Applied classical scikit-learn methods to a 2D maze environment.
        >       >     > - Position regression from RGB images (localization)
        >       >     > - - Behavioral cloning from ground-truth positions
        >       >     >   - - Behavioral cloning from raw RGB images (end-to-end)
        >       >     >    
        >       >     >     - ---
        >       >     >
        >       >     > ## Stack
        >       >     > Python · PyTorch · scikit-learn · NumPy · OpenAI Gym · Google Colab
        >       >     >
        >       >     > ## Course
        >       >     > MECS6616 — Robot Learning, Columbia University, Spring 2025
