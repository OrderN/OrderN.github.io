---
layout: default
title: "CONQUEST: Linear Scaling DFT"
published: true
---
# Welcome to the CONQUEST web site.

CONQUEST is a large scale DFT electronic structure code, capable of
both diagonalisation and linear scaling, or O(N), calculations.  It is
developed jointly by [NIMS (National Institute for Materials Science,
Japan)](http://www.nims.go.jp), [ISM (Institut des Science
Moleculaires, University of
Bordeaux)](https://www.ism.u-bordeaux.fr/?lang=en) and
[UCL](http://www.ucl.ac.uk). The code is designed to perform DFT
calculations on very large systems (containing tens of thousands,
hundreds of thousands or even millions of atoms) though is also
very fast for smaller systems, and scales exceptionally well with
numbers of processes. It can be run at
different levels of precision, ranging from *ab initio* tight binding
up to full DFT with plane wave accuracy. It is capable of operation on
a range of platforms from workstations up to high performance
computing centres. These web pages contain information on the code,
and its applications, as well as separate areas for developers.

CONQUEST is now available as an open source project under an MIT
licence.  A recent comprehensive overview has been published:
[J. Chem. Phys. **152**, 164112 (2020)](https://doi.org/10.1063/5.0005074);
a freely available copy is on [arXiv](https://arxiv.org/abs/2002.07704). 

* The source code is available [on GitHub](https://github.com/OrderN/CONQUEST-release). 
* The manual is [on ReadTheDocs](https://conquest.readthedocs.io/)

The code is presently on v1.4, released in December 2024.
It is a complete, robust code which is compatible with a very accurate
library of pseudopotentials,
[PseudoDojo](http://http://www.pseudo-dojo.org).  We welcome bug
reports and suggestions for improvement through [the GitHub issues
page](https://github.com/OrderN/CONQUEST-release/issues).  We are very
happy to welcome new users and developers.

If you are interested in more details about O(N) methods,
you can find a comprehensive review which we wrote
[here](http://stacks.iop.org/0034-4885/75/i=3/a=036503) (external
link), also available [on arXiv](https://arxiv.org/abs/1108.5976). 

You can find out more about Conquest in these pages:

* [About CONQUEST](/about.html)
   * [CONQUEST Applications](/applications.html)
   * [CONQUEST References](/references.html)
   * [CONQUEST Developers](/developers.html)
* [Using CONQUEST](/using.html)
* [All CONQUEST news stories](/news.html)
* [External Links](/links.html)

## Recent News
<ul>
  {% for post in site.posts offset: 0 limit: 5 %}
    <li><a href="{{ post.url }}">{{ post.title }}</a> ({{ post.date | date: "%B %e, %Y" }})
    <p>
      <i>{{ post.summary }}</i>
    </p>
    </li>
  {% endfor %}
</ul>
