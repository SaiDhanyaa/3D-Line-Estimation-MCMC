# 3D-Line-Estimation-MCMC

Estimate 3D line parameters from noisy 2D images using the Metropolis-Hastings MCMC algorithm with single and dual-camera inputs.

## Overview

This project employs the Metropolis-Hastings Markov Chain Monte Carlo (MCMC) algorithm to estimate the parameters of a 3D line using projections onto the (u,v) plane from one and two perspective cameras. The camera images include Gaussian noise, affecting each point along the line. By incorporating data from multiple perspectives, the project demonstrates improved parameter estimation efficiency.

## Concepts

- **Metropolis-Hastings Algorithm:** A Markov Chain Monte Carlo (MCMC) method used to generate random samples from a probability distribution, where direct sampling is challenging. The algorithm proposes new states and decides to accept or reject them based on a probability criterion.
- **Posterior Distribution:** The probability distribution of the model parameters after considering the observed data.
- **Maximum a Posteriori (MAP) Estimate:** A point estimate of the model parameters that maximizes the posterior distribution.

## Implementation Steps

1. **Initialize Parameters:** Start with initial guesses for the line's endpoints in 3D space.
2. **Iterative Sampling:** 
   - Propose new states by making small random changes.
   - Compute the acceptance ratio based on the likelihood and prior probability.
   - Accept or reject new states based on this ratio.
3. **Run the Sampler:** Use the Metropolis-Hastings sampler to generate samples from the posterior distribution.
4. **Analyze and Visualize Results:**
   - Plot the sampling progress and the Maximum a Posteriori (MAP) estimate.
   - Compare projections from single and dual-camera perspectives.

## Key Functions

- **Propose New State:** Adds Gaussian noise to the current state to generate a new proposed state.
- **Log-Likelihood Function:** Computes how probable the observed data is, given the model parameters.
- **Log-Prior Function:** Computes the prior probability of the parameters before considering the data.
- **Metropolis-Hastings Algorithm:** Iteratively proposes new states and accepts or rejects them to sample from the posterior distribution.

## Results

- **Convergence Analysis:** Convergence plots are generated to visualize the stability of the algorithm in estimating the 3D line's parameters.
- **MAP Estimation:** The Maximum a Posteriori (MAP) estimate is calculated and visualized against the observed 2D points from single and dual-camera perspectives.
- **Error Metrics:** The Root Mean Squared Error (RMSE) is computed to quantify the accuracy of the projections from each camera.

## Usage

To run this project, you need Python with the following packages:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`

### Steps to Execute

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/SaiDhanyaa/3D-Line-Estimation-MCMC.git
   cd 3D-Line-Estimation-MCMC
