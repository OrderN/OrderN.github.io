---
layout: default
title: "Using CONQUEST"
published: true
---
CONQUEST is a linear scaling DFT code which can be run at a number of
different levels of accuracy (from non-self-consistent ab initio tight
binding up to plane-wave accuracy full DFT). It features two different
basis sets (pseudo-atomic orbitals and B-splines), compatibility
with SIESTA pseudo-atomic orbitals and the ONCVPSP pseudopotentials
(e.g. the [PseudoDojo](http://www.pseudo-dojo.org) library)
and the ability to perform exact diagonalisation as
well as linear scaling solution. It runs on a wide variety of
platforms, from laptops to massively parallel systems, but requires a
parallel environment for execution. It is written in FORTRAN90 and
MPI. 

CONQUEST is now available under an open-source MIT licence as a
pre-release (for more details see
[here](blog/pre-release)) on GitHub.

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

As with all linear scaling codes, CONQUEST works well for systems with
localised electronic structure, i.e. insulators, semiconductors and
molecules. The development team has applied it to semiconductor
surfaces and biomolecules with extremely good results. 

We have also developed exact diagonalisation routines for the code,
and have invested time in k-point parallelisation and optimisation for
metallic systems. The code offers an efficient route to accurate,
exact simulations of metals. 

