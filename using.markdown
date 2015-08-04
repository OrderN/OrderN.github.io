---
layout: default
title: "Using CONQUEST"
published: true
---
CONQUEST is a linear scaling DFT code which can be run at a number of different levels of accuracy (from non-self-consistent ab initio tight binding up to plane-wave accuracy full DFT). It features two different basis sets (numerical atomic orbitals and B-splines), compatibility with SIESTA pseudo-atomic orbitals and the FHI pseudopotentials provided by ABINIT and the ability to perform exact diagonalisation as well as linear scaling solution. It runs on a wide variety of platforms, from laptops to massively parallel systems, but requires a parallel environment for execution. It is written in FORTRAN90 and MPI.
We are preparing to release the CONQUEST code freely to the academic community (under an open source licence such as the [GNU General Public Licence](http://www.gnu.org/copyleft/gpl.txt)). As part of this preparation, we are seeking beta release testers who will have early access to the code under a collaborative agreement with the CONQUEST development team. The beta release has finished the first phase (limited release to a few groups) and is now widening to more groups, who will be given access to the code and support from the CONQUEST development team. At least one publication resulting from this phase needs to be joint.

The groups using CONQUEST around the world are based in:

* UCL, London, UK
* NIMS, Tsukuba, Japan
* RIKEN, Japan
* Osaka University, Japan
* Tottori University, Japan
* Bordeaux University, France
* Army Research Labs, USA
* Spanish National Cancer Research Centre
* Tokyo University of Science, Japan

After successful beta testing, the code will be released without restriction (beyond the GPL licence) though significant technical support will not be offered without some form of collaboration. We plan to offer workshops and tutorials to assist users in using CONQUEST.

As with all linear scaling codes, CONQUEST works well for systems with localised electronic structure, i.e. insulators, semiconductors and molecules. The development team has applied it to semiconductor surfaces and biomolecules with extremely good results.

We have also developed exact diagonalisation routines for the code, and have invested time in k-point parallelisation and optimisation for metallic systems. The code offers an efficient route to accurate, exact simulations of metals.

If you would like to be considered for inclusion in the beta testing programme, please contact one of the management team (given below) with a description of the problems you are working on, and of the computational resources available to you.

* David Bowler david.bowler at ucl.ac.uk
* Tsuyoshi Miyazaki MIYAZAKI.Tsuyoshi at nims.go.jp
