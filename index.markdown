---
layout: default
title: "CONQUEST: Linear Scaling DFT"
published: true
---
# Welcome to the CONQUEST web site.

CONQUEST is a large scale DFT electronic structure code, capable of
both diagonalisation and linear scaling, or O(N), calculations. 
It has been developed jointly by [NIMS (National Institute for Materials Science,
Japan)](http://www.nims.go.jp) and [UCL](http://www.ucl.ac.uk). The
code is designed to perform DFT calculations on very large systems
(containing tens of thousands, hundreds of thousands or even millions
of atoms). It can be run at different levels of precision, ranging
from *ab initio* tight binding up to full DFT with plane wave
accuracy. It is capable of operation on a range of platforms from
workstations up to high performance computing centres. These web pages
contain information on the code, and its applications, as well as
separate areas for developers. 

CONQUEST is now available as an open source project under an MIT
licence.  A recent comprehensive overview is available on
[arXiv](https://arxiv.org/abs/1907.05768). 

* The source code is available [on GitHub](https://github.com/OrderN/CONQUEST-release). 
* The manual is [on ReadTheDocs](https://conquest.readthedocs.io/)

While it is a complete, robust code, we are designating this release
as a pre-release, as there are some changes that will be made over the
next few months to improve the user-friendliness of the code. 

At present, we are looking for early adopters to use the code, submit
bug reports and suggestions improvement.  We particularly welcome new
developers of the code.  The present roadmap for the code can be seen
on [the GitHub issues page](https://github.com/OrderN/CONQUEST-release/issues).

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
