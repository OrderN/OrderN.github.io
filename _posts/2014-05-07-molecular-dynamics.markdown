---
layout: post
title: Molecular dynamics
published: true
year: 2014
month: 5
day: 7
summary: Implementation of efficient, O(N) MD in CONQUEST
---
Michiaki Arita and Tsuyoshi Miyazaki of NIMS have successfully adapted CONQUEST
so that molecular dynamics is possible. In recent tests they have shown that
picoseconds of linear scaling MD can be performed with energy conserved.
A paper is in preparation, and the first part of the code has been committed as r137.

Update, 2014-11-11: The research has been published[1], and shows linear scaling up to
32,768 atoms. It is also available on [arXiv](https://arxiv.org/abs/1409.6085)

[1] J. Chem. Theor. Comput. **10**, 5419 (2013) [DOI:10.1021/ct500847y](http://dx.doi.org/10.1021/ct500847y)
