# Model Extraction Extensions – SSE Project (CS6570)

This repository contains the code and documentation for a course project done as part of the Secure Systems Engineering (CS6570) course, taught by Prof. Chester Rebeiro at IIT Madras in the 2025 even semester.

## Team Details

**Team Name**: Comfortably_Dumb  
**Team Members**:

- Pranay Mathur (EE22B132)
- Varun Bajpai (EE22B152)

## Overview

The goal of this project was to extend a known model extraction attack to cover a broader class of neural networks, including those with:

- Activation functions other than ReLU (LeakyReLU, Tanh, Sigmoid)
- Multi-class outputs instead of binary classification

Our implementation builds on the original attack and adapts it for these new scenarios.

## Repository Structure

This repository includes several Python scripts that implement the attack for different network types:

- `verify_1_deep_nn_attack_leaky.py`: For models using LeakyReLU activation. Depends on `utils_leaky.py`.
- `verify_1_deep_nn_attack_tanh.py`: For models using Tanh activation. Depends on `utils_tanh.py`.
- `verify_1_deep_nn_attack_sig.py`: For models using Sigmoid activation. Depends on `utils_sig.py`.
- `verify_1_deep_nn_attack_multi_class.py`: For models with multi-class outputs. Depends on `utils.py`.

Each script carries out the full attack pipeline for its respective case.

## Model Generation

We used a Python notebook `Model_Train.ipynb` to generate and save neural network models for testing. You can modify or extend this notebook to create new models for experimentation.

## Saved Models

The directory includes models trained with different activation functions:

- LeakyReLU model : `leaky_mnist_hidden2_1.npz` and `leaky_mnist_hidden2_2.npz`
- Tanh model : `tanh_mnist_hidden2_1.npz` and `tanh_mnist_hidden2_2.npz`
- Sigmoid model : `sigmoid_mnist_hidden2_1.npz` and `sigmoid_mnist_hidden2_2.npz`
- Multi-class output model : `relu_2_class.npz`

## Extracted Models

- LeakyReLU models: `leaky_1_784_2_1.npz` and `leaky_2_784_2_1.npz`
- Tanh models: `tanh_1_784_2_1.npz` and `tanh_2_784_2_1.npz`
- Sigmoid models: `sigmoid_1_784_2_1.npz` and `sigmoid_2_784_2_1.npz`
- Multi-class output model: `relu_2_classes_784_2_1.npz`
- ReLU (baseline) model: `relu_784_2_1.npz`

## Report

The theoretical background, methodology, and results of the project are detailed in the report file:

- `SSE_Project_report.pdf`

This document explains how the attack was adapted for each case and summarizes the findings.

## How to Use

To test the attack, make sure you have Python 3.8+ and the necessary packages installed. Then, run the relevant script depending on the model you're targeting. For example:

```bash
python verify_1_deep_nn_leaky.py
```
