---
layout: default
title: "CONQUEST: Linear Scaling DFT"
published: true
---
# Welcome to the Conquest web site.

Conquest is a linear scaling, or O(N), DFT electronic structure code developed jointly by [NIMS (National Institute for Materials Science, Japan)](http://www.nims.go.jp) and [UCL](http://www.ucl.ac.uk). The code is designed to perform DFT calculations on very large systems (containing tens of thousands, hundreds of thousands or even millions of atoms). It can be run at different levels of precision, ranging from *ab initio* tight binding up to full DFT with plane wave accuracy. It is capable of operation on a range of platforms from workstations up to high performance computing centres. These web pages contain information on the code, and its applications, as well as separate areas for developers.

We have recently written a comprehensive review of O(N) methods, which you can find [here](http://stacks.iop.org/0034-4885/75/i=3/a=036503) (external link).

You can find out more about Conquest in these pages:

* [About CONQUEST](/about.html)
   * [CONQUEST Applications](/applications.html)
   * [CONQUEST References](/references.html)
   * [CONQUEST Developers](/developers.html)
* [Using CONQUEST](/using.html)
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
