**Authors:** Valentina Perez, Cesar Hoyos, Sebastian Montoya

**Date:** March 2022

# Spectral Analysis Notebook

This Jupyter Notebook contains code for the analysis of optical spectra obtained from an Ocean Optics 2000 spectrometer. The notebook includes data loading, data processing, and visualization steps. The main goals of this analysis are to calculate reflectance, compare experimental and theoretical values, and apply the Kramer-König relations and TAUC plots to extract material properties.

## Getting Started

To run the notebook successfully, make sure you have the required Python libraries installed. You can install them using `pip` or `conda`. Here are the libraries used in this notebook:

- `pandas`: For data loading and manipulation.
- `numpy`: For numerical operations.
- `matplotlib`: For data visualization.

## Data Loading

The code begins by loading data from the Ocean Optics 2000 spectrometer, including dark signals and sample signals for both the reference and the material under study (Si). It then applies median filtering to the signals to reduce noise and calculates reflectance.

## Theoretical Data

Theoretical data for the refractive index (n) and extinction coefficient (k) of the material (Si) is loaded. The code calculates theoretical reflectance (R) from the provided n and k values.

## Experimental vs. Theoretical Reflectance

The code generates a plot to compare the experimental and theoretical reflectance values. This visualization allows you to assess how well the experimental data matches the theoretical predictions.

## Refractive Index and Extinction Coefficient (n and k)

Another plot is created to display the refractive index (n) and extinction coefficient (k) of the material. This provides insight into the optical properties of the material based on theoretical data.

## Kramer-König Relations

The code applies the Ohta algorithm with the McLaurin method to calculate k as a function of theoretical n and compare it with the expected k. A plot is generated to visualize the results, allowing you to assess the accuracy of the Kramer-König relations for your material.

---

This README provides an overview of the code and its main functions. The Jupyter Notebook itself contains detailed code and comments for a more in-depth understanding of the analysis.


## Diffuse Reflectance

Diffuse reflectance refers to the amount of light that is uniformly reflected from a surface in all directions when illuminated. It plays a significant role in various applications, such as surface characterization, where it provides insights into texture, brightness, and uniformity. Additionally, the food industry utilizes diffuse reflectance to assess the quality and maturity of food products.

From the interaction between incident light and a sample, we can establish a mathematical relationship between intensities:

\[
I_0 = I_a + I_t + I_r + I_s \quad \text{(1)}
\]

Where:
- \(I_0\) is the incident beam intensity,
- \(I_a\) is the absorbed intensity,
- \(I_t\) is the transmitted intensity,
- \(I_s\) is the intensity due to the scattering process, and
- \(I_r\) is the specularly reflected intensity.

By using Equation (1), we can calculate the diffuse reflectance (\(R_\infty\)) based on the relationship between the incident intensity (\(I_0\)) and the scattering intensity (\(I_s\)):

\[
R_\infty = \frac{I_0}{I_s} \quad \text{(2)}
\]

Experimental measurements of diffuse reflection are typically performed using an integrating sphere, which scatters incident light in all directions. The sphere's inner surface is coated with a high-diffuse reflection material, and information is collected through a small aperture with a detector.

## Kubelka-Munk Function

The Kubelka-Munk equation is a valuable tool when studying opaque samples composed of various particle sizes. It establishes a relationship between the reflectance and transmittance of the sample. Mathemematically, the Kubelka-Munk function (\(F_{R_\infty}\)) is expressed as:

\[
F_{R_\infty} = \frac{(1-R_\infty)^2}{2R_\infty} \quad \text{(3)}
\]

Moreover, Equation (3) can be used to create a graphical representation of optical absorption as a function of the incident photon energy within a material. This provides information about the material's band gap energies. The relationship is given by Equation (4):

\[
(F_{R_\infty} \cdot h\nu )^{1/\gamma} = h\nu - E_g \quad \text{(4)}
\]

Here, \(\gamma = 1/2\) for direct transitions and \(\gamma = 2\) for indirect transitions.

Experimentally, various materials exhibit specific band gap ranges. For example, perovskite has a band gap in the range of \(1.2-2.3\) eV, titanium dioxide falls in the \(2.3-3\) eV range, and zinc oxide has a band gap of approximately 3.37 eV [4-6].

...
