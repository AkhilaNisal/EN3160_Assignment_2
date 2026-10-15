# EN3160 - Assignment 02: Image Processing and Computer Vision

**Department of Electronic and Telecommunication Engineering**  
**University of Moratuwa**

Implementation and experimental analysis of classical computer vision algorithms using **Python, OpenCV, NumPy, SciPy, and Matplotlib**.

## Overview

This assignment explores fundamental image processing and computer vision techniques, emphasizing geometric estimation, feature extraction, robust model fitting, and image alignment.

The work investigates how mathematical models and local image features can be used to identify corresponding structures across images, estimate transformations, and handle noisy data and mismatched features.

The implementations, intermediate visualizations, and experimental results are provided in the Jupyter notebook.

## Main Concepts and Experiments

### 1. Image Processing and Geometric Analysis

Exploration of image processing operations and geometric relationships using numerical methods.

Key concepts include:
- Image representation and manipulation
- Geometric transformations
- Numerical computation and visualization
- Analysis of image structures and spatial relationships

### 2. Model Fitting and Robust Estimation

Investigation of methods for estimating geometric models from observed data.

**Ordinary Least Squares (OLS)**
- Minimizes squared residual errors.
- Provides a baseline for geometric model fitting.

**Total Least Squares (TLS)**
- Considers errors in multiple coordinate directions.
- Uses Singular Value Decomposition (SVD) to estimate model parameters.
- Suitable for orthogonal-distance line fitting.

**Random Sample Consensus (RANSAC)**
- Randomly samples minimal subsets of observations.
- Estimates candidate models.
- Identifies inliers based on residual errors.
- Selects robust estimates in the presence of outliers.

These methods illustrate the importance of robust estimation when working with noisy measurements.

### 3. Feature Detection and Matching

Exploration of local image features and correspondence estimation.

Key techniques:
- Detection of distinctive image keypoints
- Extraction of feature descriptors
- Descriptor matching using distance-based methods
- Nearest-neighbor matching
- Lowe's ratio test for rejecting ambiguous matches
- Visualization and analysis of feature correspondences

The experiments demonstrate how local image features can support matching between images captured under different viewing conditions.

### 4. Homography Estimation and Image Alignment

Implementation of feature-based image alignment using SIFT, descriptor matching, and RANSAC.

**Processing Pipeline**

1. Load the reference and target images.
2. Convert images to grayscale.
3. Detect SIFT keypoints and compute descriptors.
4. Establish candidate correspondences using a brute-force matcher.
5. Apply Lowe's ratio test to reject ambiguous matches.
6. Estimate the homography matrix using RANSAC.
7. Transform image coordinates and visualize alignment results.

A planar projective transformation is represented by:

\[
\begin{bmatrix}
x'\\
y'\\
1
\end{bmatrix}
\sim
H
\begin{bmatrix}
x\\
y\\
1
\end{bmatrix}
\]

where \(H\) is a \(3 \times 3\) homography matrix.

This experiment demonstrates how feature correspondence and robust geometric estimation can be combined to align images obtained from different perspectives.

## Technologies Used

- **Python** – Main programming language
- **OpenCV** – Image processing, SIFT, feature matching, and homography estimation
- **NumPy** – Matrix operations and numerical computations
- **SciPy** – Numerical optimization and scientific computing
- **Matplotlib** – Visualization of images, features, and experimental results
- **Jupyter Notebook** – Implementation and documentation

## Repository Structure

```text
EN3160_Assignment_2/
│
├── EN3160_Assignment_02.ipynb
│
├── a2images/
│   └── Input images
│
├── Q4_results/
│   └── Image alignment results
│
├── Q3_Result_1.jpg
├── Q3_Result_2.jpg
├── Q3_Stages_2.png
│
├── en3160_assignment_02 (1).pdf
├── .gitignore
└── README.md
```

## Running the Notebook

### 1. Clone the Repository

```bash
git clone https://github.com/AkhilaNisal/EN3160_Assignment_2.git

cd EN3160_Assignment_2
```

### 2. Install Dependencies

```bash
pip install numpy scipy matplotlib opencv-python jupyter ipykernel
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook EN3160_Assignment_02.ipynb
```

Run the notebook cells sequentially, ensuring that the input image paths match the local repository structure.

## Experimental Results

The repository includes intermediate and final results demonstrating the operation of computer vision algorithms.

### Question 3 – Experimental Visualizations

The saved visualizations include:

- [Result 1](Q3_Result_1.jpg)
- [Result 2](Q3_Result_2.jpg)
- [Processing Stages](Q3_Stages_2.png)

### Question 4 – Image Alignment Results

Generated results are available in the [Q4_results](Q4_results/) directory.

These experiments illustrate the use of local feature matching and geometric transformations for image correspondence and alignment.

## Key Learning Outcomes

- Understanding geometric model fitting using least-squares methods
- Applying SVD to numerical estimation problems
- Using RANSAC to improve robustness against outliers
- Detecting and describing local image features using SIFT
- Matching features across different images
- Understanding homography estimation and projective transformations
- Building image alignment pipelines using OpenCV

## Author

**Akhila Nisal Wedamestrige**  
Electronic and Telecommunication Engineering Undergraduate  
University of Moratuwa

GitHub: [AkhilaNisal](https://github.com/AkhilaNisal)

---

*Academic coursework – EN3160: Image Processing and Machine Vision, University of Moratuwa.*
