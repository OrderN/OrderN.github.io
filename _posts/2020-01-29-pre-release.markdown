---
layout: post
title: Conquest available in pre-release
published: true
year: 2020
month: 1
day: 29
summary: Conquest is available under an open-source licence
---
We are happy to announce that CONQUEST, a large scale DFT code, is now
available as an open source project (MIT licence).  While it is a
complete, robust code, we are designating this release as a
pre-release, as there are some changes that will be made over the next
few months to improve the user-friendliness of the code. 

At present, we are looking for early adopters to use the code, submit
bug reports and suggestions improvement.  We particularly welcome new
developers of the code.  The present roadmap for the code can be seen
on the GitHub issues page. 

The full release (v1.0) of CONQUEST will mainly involve improved
output and tutorials being provided, at which point it will be
suitable for all users. 

The capabilities of CONQUEST at present include:

* Static total energy calculations
* Structural relaxation (L-BFGS, CG, FIRE, QMD)
* NVE and NVT MD (Stochastic Velocity Rescaling and Nose-Hoover Chains)
* Cell optimisation (CG)
* PAO basis sets (full library for LDA, PBE and PBEsol supplied, along with generation utility)
* Multi-site support function (MSSF) basis sets with self consistency for large scale calculations
* O(N) calculations with SZ or SZP basis sets
* Electronic structure: DOS, charge density and band output
* Integration with ASE

The release is available [here](https://github.com/OrderN/CONQUEST-release).
