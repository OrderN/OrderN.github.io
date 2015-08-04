---
layout: default
title: "About CONQUEST"
published: true
---
This page gives a high level overview of the ideas underlying linear scaling
codes, and Conquest in particular. Technical details of the Conquest code can
be found in the [CONQUEST References](/references.html) section of these
web pages; a reprint giving details of recent Conquest developments is
available [here](/papers/pssb_preprint.pdf).

* [Introduction](#S1)
* [Density matrices](#S2)
* [Sparse matrices and parallel scaling](#S3)
* [Support functions](#S4)
* [Other technical details](#S5)

### Introduction
<a name="S1"></a>
Normal DFT codes solve for the Kohn-Sham eigenstates
( \\(\hat{H} \psi_n = \epsilon_n \psi_n\\) ); these eigenstates extend throughout the
simulation cell. Additionally, the eigenstates must be kept orthogonal to each
other, which involves integrals of the form
\\(\int \mathrm{d}\mathbf{r} \psi_n(\mathbf{r}) \psi_m(\mathbf{r})\\). These
integrals contain three terms which scale with the simulation cell size, and
hence with the number of atoms in the cell, giving \\(\mathcal{O}(N^3)\\) scaling.
This dominates as system size increases, and there is a practical limit of a
thousand atoms or so, even on high performance computing (HPC) machines.

Linear scaling DFT codes, by contrast, take advantage of the well-known fact
that electronic structure is local. Rather than solve for the eigenstates,
most linear scaling codes solve for the density matrix
\\(\rho(\mathbf{r},\mathbf{r}^\prime)\\). This is forced to be local in space
(i.e. setting \\(\rho(\mathbf{r},\mathbf{r}^\prime) = 0, \vert\mathbf{r} - \mathbf{r}^\prime\vert > R_c\\)
for some cutoff distance $R_c$). Then, provided that the implementation is
performed carefully, the computer effort and memory will scale linearly with
the number of atoms: \\(\mathcal{O}(N)\\) scaling.

### Density Matrices
<a name="S2"></a>
For practical implementation, the density matrix is assumed to be separable,
  and is written in terms of localised, atom-centred support functions:
\\[\rho(\mathbf{r},\mathbf{r}^\prime) = \sum\_{i\alpha j\beta} \phi\_{i\alpha}(\mathbf{r}) K\_{i\alpha j\beta} \phi\_{j\beta}(\mathbf{r}^\prime)\\]

  The support functions then define Hamiltonian and overlap matrices
  (\\(H\_{i\alpha j\beta}\\) and \\(S\_{i\alpha j\beta}\\)). The ground state search
  now goes over the density matrix and the support functions, with the usual
  constraint on self-consistency between potential and charge density. Instead
  of requiring orthonormality between the eigenstates, the density matrix is
  required to be idempotent (i.e. \\(\rho^2 = \rho\\)). This is not an easy
  condition to impose, and there are various solutions. Conquest works by
  writing \\(K = 3LSL - 2LSLSL\\), a transformation which has extrema at 0 and 1,
  which is due to McWeeny.

### Sparse matrices and parallel scaling
<a name="S3"></a>

  In order to have linear scaling both in computational time and memory,
  linear scaling codes must use different techniques to normal codes. In
  particular, the matrices used will be sparse (that is they will have a
  limited number of non-zero elements) but linear scaling will not happen
  unless the zero elements are eliminated. Conquest has specially designed
  sparse matrix techniques, which are also constructed to give good performance
  on massively parallel computers.

  If a linear scaling code is to operate on thousands or millions of atoms,
  then it must operate on parallel machines. The spatial locality of linear
  scaling methods (all operations relating to a given atom are restricted to a
  local area of real space) makes them naturally parallelisable. In Conquest,
  each processor (or each core in the multi-core machines which are becoming
  common) is given responsibility for a different group of atoms (known as a
  bundle of atoms). The rows of matrices labelled by these atoms are stored
  on the core, and when matrix multiplications are performed the core is
  responsible for calculating the rows of the new matrix.

### Support functions
<a name="S4"></a>

  The support functions \\(\phi\_{i\alpha}(\mathbf{r})\\) are represented in terms
  of basis functions: \\(\phi\_{i\alpha}(\mathbf{r}) = \sum\_s c\_{i\alpha s} \chi\_s(\mathbf{r})\\).
  In Conquest, there are two basis functions implemented:

* Blip functions or b-splines, which allow plane-wave accuracy to be achieved
* Pseudo-atomic orbitals (PAOs), which allow rapid, analytic calculations

  If a limited set of PAOs is used, then Conquest operates as an ab initio
  tight binding (or tight binding DFT) code, either self-consistent or
  non-self-consistent. As the set of PAOs expands, or for blip function basis
  sets, then full DFT is recovered, and plane-wave accuracy can be achieved by
  increasing cutoffs on the support functions and the density matrix.

### Other technical details
<a name="S5"></a>

The charge density is stored on a grid, which is also used for numerical
integrals and FFTs. As with the atoms, each processor or core is given
responsibility for a specific area of the integration grid. The operation of
Conquest is most efficient if these areas overlap strongly and are compact.
