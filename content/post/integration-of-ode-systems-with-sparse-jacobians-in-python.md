---
title: "Integration of ODE systems with sparse Jacobians in Python"
id: 10
categories:
  - "Modeling"
tags:
  - "Python"
date: "2015-09-07 10:12:45"
banner: "/images/matrix.jpg"
---

The Centre for Plant Integrative Biology (CPIB, University of Nottingham) has developed a Python module based on the Fortran library ODEPACK to integrate ODE systems with sparse Jacobian matrices. It is quite similar in usage to the odeint function from Scipy.

1.  Download "SimuPlant Server" from [http://www.simuplant.org](http://www.simuplant.org).
2.  Open the archive.
3.  Extract the "odesparse_1" folder. This is all we need.
4.  Move to the extracted "odesparse_1" folder and install the module.
<pre> python setup.py install</pre>
You will need a Fortran compiler.
5.  You can then import the "odesparse" module in Python. To integrate ODEs, use the "odesparse.odeints" function. You can refer to the "README" file in the "odesparse_1" folder for the exact usage, which slightly differs from "odeint" in Scipy.
6.  One important feature of odeints is that it takes the keyword argument "JPat", which enables you to provide the structure (matrix of 0s and 1s) of the Jacobian matrix, as a Scipy sparse matrix (e.g.: lilmatrix or csr).

<small>Banner photo by [Pai Shih](http://www.flickr.com/photos/30939981@N00/15850989974) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by/2.0/ "Attribution License")</small>