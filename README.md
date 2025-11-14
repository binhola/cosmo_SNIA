# Cosmic SNIA Analysis

This is a student project focused on the analysis of Type Ia Supernovae (SNIA) data to study cosmological parameters and the expansion of the universe.

The primary analysis is conducted in the `SNIA_analysis.ipynb` Jupyter Notebook.

## Project Overview

The notebook covers the following key steps:
1.  **Data Loading**: Imports supernova data, including redshift, apparent magnitude, and other parameters.
2.  **Cosmological Model**: Defines a function to calculate the apparent magnitude based on a `LambdaCDM` cosmological model using `astropy`.
3.  **Hubble Diagram**: Plots the initial Hubble diagram (apparent magnitude vs. redshift).
4.  **Model Fitting**: Uses `scipy.optimize.curve_fit` to find the best-fit cosmological parameters ($\Omega_m^0$, $\Omega_\Lambda^0$) and the absolute magnitude ($M_B$).
5.  **Residual Analysis**: Calculates and plots the residuals of the fit to assess its quality.
6.  **Magnitude Correction**: Investigates and applies corrections to the apparent magnitude based on supernova color (`color`) and stretch (`x1`) to reduce systematic biases.
7.  **Likelihood Analysis**: Explores the parameter space by computing and plotting the likelihood function for cosmological parameters, including 2D contour plots for $\Omega_m^0$ vs. $\Omega_\Lambda^0$.

## Setup and Installation

To run this analysis, you'll need Python 3 and the libraries listed in `requirements.txt`.

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/binhola/cosmo_SNIA.git
    cd cosmic_SNIA
    ```

2.  **Create a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

Once the setup is complete, you can run the analysis using Jupyter:

1.  **Start the Jupyter server:**
    ```bash
    jupyter notebook
    ```
    or
    ```bash
    jupyter lab
    ```

2.  **Open the notebook:**
    In the Jupyter interface in your browser, open the `SNIA_analysis.ipynb` file and run the cells.

## Data

The data for this project is located in `data/sne_data_zsorted.txt` and is based on the SNLS collaboration (Betoule et al. 2014). It contains measurements for 740 Type Ia supernovae.
