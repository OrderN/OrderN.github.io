---
layout: post
title: Hyper-parameters for machine learning forces
published: true
year: 2023
month: 06
day: 05
summary: CONQUEST is used to provide ab initio MD data for improved fitting of machine learning forces
---
The atomic descriptors used in machine learning to predict forces are
often high dimensional. In general, by retrieving a significant amount
of structural information from these descriptors, accurate force
predictions can be achieved. On the other hand, to acquire higher
robustness for transferability without overfitting, sufficient
reduction of descriptors should be necessary. In this study, we
propose a method to automatically determine hyperparameters in the
atomic descriptors, aiming to obtain accurate machine learning forces
while using a small number of descriptors. Our method focuses on
identifying an appropriate threshold cut-off for the variance value of
the descriptor components. To demonstrate the effectiveness of our
method, we apply it to crystalline, liquid, and amorphous structures
in SiO2, SiGe, and Si systems. By using both conventional two-body
descriptors and our introduced split-type three-body descriptors, we
demonstrate that our method can provide machine learning forces that
enable efficient and robust molecular dynamics simulations.

The paper is published in [Phys. Chem. Chem. Phys. 25, 17978 (2023)](https://doi.org/10.1039/D3CP01922E).
