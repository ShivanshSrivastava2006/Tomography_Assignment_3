# Tomography Assignment 3
# Scalable Quantum Tomography Surrogate

This repository contains a scalable surrogate model for quantum state tomography,
with serialization, benchmarking, and ablation studies.

## Contents
- `Assignment_3.ipynb`: main notebook
- `models/`: serialized checkpoints
- `results/`: CSV summaries
- `figures/`: plots

## How to run
```bash
pip install -r requirements.txt
jupyter notebook
```
# Tomography Assignment 4

## Contents
> Only `Assigment_4.ipyb`

## Objective

Build a lightweight machine learning classifier that automatically identifies the type of single-qubit noise channel from its mathematical representation. Specifically, we distinguish between:
- Depolarizing channel
- Amplitude damping channel
- The goal is to simulate a fast calibration-time diagnostic tool for quantum hardware.

What We Are Doing (Step-by-Step)

### Generate Synthetic Quantum Channels
```
- We construct parameterized noise models using their Kraus operators:
- Depolarizing channel with varying noise strength p
- Amplitude damping channel with varying damping rate γ

These represent realistic quantum noise processes.
```
### Convert Channel to Feature Vector
```
Each channel is converted to its Choi matrix representation.
Why?
Because:
The Choi matrix uniquely represents a quantum channel.
It gives us a fixed-size numerical object suitable for ML.
After this we:
- Flatten the real part
- Flatten the imaginary part
- Concatenate both into one feature vector
This transforms a quantum object into a classical ML feature vector.
```
### Build Dataset
> We create a labeled dataset

### Train Classifier
We train a Logistic Regression model to classify the feature vectors.
Steps:
> Train/validation split
> Fit model
> Evaluate accuracy

### Test on New Channels
We generate unseen channels and check if the classifier correctly identifies them.
This simulates how the model would behave during a calibration loop.


