# Comparative Analysis of Computer Vision Architectures for Reinforcement Learning Agents in ViZDoom

**Course:** CMP722 - Advanced Computer Vision  
**Author:** Mehmet Yusuf Bilge

## Overview

This project investigates the relationship between computer vision model architectures and the performance of reinforcement learning (RL) agents in ViZDoom, a first-person shooter simulation environment. Different deep learning models are integrated as visual perception modules within the same RL framework to measure their impact on agent performance.

Traditional RL agents in ViZDoom typically rely on simple convolutional encoders to interpret pixel input. This project explores whether more advanced vision architectures (such as YOLO) can enhance scene understanding and improve learning efficiency compared to baseline CNN encoders.

## Objectives

- Implement and compare multiple deep learning-based vision architectures (CNN, YOLO, etc.) for perception in ViZDoom.
- Integrate each model with the same reinforcement learning algorithm (PPO) to ensure fair comparison.
- Train agents to perform navigation or combat tasks using visual input.
- Evaluate models based on detection accuracy (mAP, IoU, precision/recall) and RL performance metrics (reward per episode, learning speed, survival time).
- Analyze trade-offs between model complexity, training time, perception accuracy, and gameplay performance.

## Methodology

### Environment and Data

- **Environment:** ViZDoom API
- **Task:** Object detection and agent training (detecting enemies, health packs, weapons)
- **Data:** Frames extracted from gameplay, optionally annotated for supervised pretraining
- **Preprocessing:** Image resizing, normalization, frame skipping, and data augmentation

### Models

- **CNN-based encoder:** A baseline 3-layer convolutional network that processes raw screen frames into latent embeddings for the RL policy.
- **YOLO-based detector:** An object detection model that provides structured scene understanding (bounding boxes, class labels) as input to the RL agent.
- Additional architectures may be included as time permits.

### Reinforcement Learning

All vision models are paired with the same RL algorithm (PPO via Stable-Baselines3). Hyperparameters such as learning rate, batch size, and exploration policy are kept constant across experiments to ensure a fair comparison.

### Evaluation

- **Vision Metrics:** mAP, IoU, precision, recall
- **RL Metrics:** Average reward per episode, convergence rate, survival time
- **Comparative Analysis:** Impact of each visual model on agent performance, efficiency, interpretability, and training stability

## Tech Stack

- Python
- PyTorch
- ViZDoom
- Stable-Baselines3
- Ultralytics YOLO

## References

- Kempka, M. et al. (2016). ViZDoom: A Doom-based AI Research Platform for Visual Reinforcement Learning. IEEE Conference on Computational Intelligence and Games.
- Schulman, J. et al. (2017). Proximal Policy Optimization Algorithms. arXiv:1707.06347.
- Redmon, J. et al. (2016). You Only Look Once: Unified, Real-Time Object Detection. CVPR.
- Stable-Baselines3: https://github.com/DLR-RM/stable-baselines3

## License

This project is developed for academic purposes as part of the CMP722 course.
