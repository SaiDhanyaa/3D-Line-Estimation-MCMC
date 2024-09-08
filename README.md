# 3D-Line-Estimation-MCMC

![Python](https://img.shields.io/badge/python-3.x-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![MCMC](https://img.shields.io/badge/MCMC-Metropolis--Hastings-red)

This repository contains a project that employs the Metropolis-Hastings Markov Chain Monte Carlo (MCMC) algorithm to estimate the parameters of a 3D line from noisy 2D images captured by one or two cameras. The project demonstrates the efficiency and accuracy of parameter estimation when using data from multiple camera perspectives.

## Project Overview

The primary goal of this project is to estimate the parameters of a 3D line using projections onto the (u,v) plane from one and two perspective cameras, where each point along the line is affected by Gaussian noise. The Metropolis-Hastings MCMC algorithm is used to infer the line parameters by maximizing the posterior distribution based on the observed noisy data.

## Methodology

The project involves the following steps:

1. **Data Generation**: 
   - Generate 2D projections of a 3D line with added Gaussian noise.
   - Create data for both single and dual-camera perspectives.
   
2. **Metropolis-Hastings MCMC Algorithm**: 
   - Initialize the parameters for the 3D line.
   - Iteratively propose new parameter values and compute the acceptance ratio.
   - Update the parameters based on the acceptance criterion to approximate the posterior distribution.

3. **Results Analysis**:
   - Compare the results of the estimation using single and dual-camera inputs.
   - Visualize the convergence of the algorithm and the estimated 3D line parameters.

## Files in the Repository

- **`3d_line_estimation_mcmc.py`**: Python script containing the full implementation of the MCMC algorithm, including data generation, parameter estimation, and visualization.
- **`data/`**: Directory containing sample data files (`inputs.csv`, `points_2d_camera_1.csv`, `points_2d_camera_2.csv`).
- **`results/`**: Directory to store output plots, convergence results, and MAP estimates.
- **`README.md`**: Project overview and setup instructions.
- **`LICENSE`**: MIT License file.

## Installation

### Requirements

To run this project, you need:

- Python 3.x
- Python libraries:
  - numpy
  - pandas
  - matplotlib

### Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/SaiDhanyaa/3D-Line-Estimation-MCMC.git
    cd 3D-Line-Estimation-MCMC
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Ensure all necessary input files are present in the `data/` directory.
2. Run the Python script to execute the MCMC algorithm:
    ```bash
    python 3d_line_estimation_mcmc.py
    ```
3. View the output results and plots stored in the `results/` directory.

## Results

- **Convergence Analysis**: The convergence of the algorithm is visualized to assess its stability in estimating the 3D line parameters.
- **MAP Estimation**: The Maximum a Posteriori (MAP) estimate is calculated and plotted against the observed 2D points.
- **Error Metrics**: The Root Mean Squared Error (RMSE) quantifies the accuracy of the parameter estimates.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## References

1. **Metropolis-Hastings Algorithm** - A Markov Chain Monte Carlo (MCMC) method for generating random samples from a probability distribution.

## Contributing

Contributions are welcome! If you would like to contribute, please fork the repository and use a feature branch. Pull requests are gladly accepted.

## Acknowledgments

Special thanks to the University of Arizona for providing the resources and support to work on this project.

## Contact

For any questions or feedback, please contact [Dhanyapriya Somasundaram](mailto:dhanyapriyas@arizona.edu).
