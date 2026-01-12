# GWO-ICE: Grey Wolf Optimization for Image Contrast Enhancement

This repository contains the implementation of a metaheuristic-based approach to automated image contrast enhancement. The project utilizes the Grey Wolf Optimizer (GWO) to identify optimal transformation parameters that maximize image entropy and structural detail.

## Abstract
Image enhancement via global transformations often suffers from over-saturation or artifact introduction. This study implements the Grey Wolf Optimization algorithm—a swarm intelligence technique—to search the parameter space of non-linear enhancement functions. By simulating the leadership hierarchy and hunting mechanisms of grey wolves, the algorithm converges on a parameter set that balances brightness preservation with contrast expansion.

## Objective
The primary goal is to benchmark the performance of GWO against traditional deterministic methods, such as Contrast Limited Adaptive Histogram Equalization (CLAHE), using objective image quality assessment (IQA) metrics.

## Technical Implementation
- **Algorithm:** Grey Wolf Optimizer (GWO)
- **Primary Metrics:** Discrete Entropy, Peak Signal-to-Noise Ratio (PSNR), and Structural Similarity Index (SSIM).
- **Environment:** Python 3.9+, OpenCV, NumPy.

## Repository Structure
- `src/`: Source code for the GWO engine and image processing pipeline.
- `data/`: Sample dataset for testing (Low-light and low-contrast imagery).
- `benchmarks/`: Comparative analysis scripts against GHE and CLAHE.
- `docs/`: Formal technical report and mathematical derivation of the objective function.

## Mathematical Logic
The optimization is driven by the social hierarchy of the pack:
- **Alpha ($\alpha$):** The current fittest solution (highest objective function value).
- **Beta ($\beta$):** The second fittest solution.
- **Delta ($\delta$):** The third fittest solution.
- **Omega ($\omega$):** The remaining candidate solutions updated based on the positions of $\alpha$, $\beta$, and $\delta$.


## Evaluation Methodology
Enhancement quality is evaluated through:
1. **Entropy Maximization:** Increasing the information content within the processed frame.
2. **Edge Intensity Analysis:** Ensuring structural edges are sharpened without introducing noise.
3. **Computational Efficiency:** Measuring convergence speed across varying population sizes.

---
**Author:** Nimit Ahluwalia  
**Project Type:** Independent Research (Computer Vision / Optimization)
