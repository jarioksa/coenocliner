coenocliner
===========

An R package to simulate species abundances (counts) along gradients

One of the key ways quantitative ecologists attempt to understand the 
properties and behaviour of the methods they use or dream up is 
through the use of simulated data. There are a number of computer 
programmes for simulating ecological data along gradients, such as 
Peter Minchin's COMPAS, but none (that I am aware of) that are 
available for R on CRAN. Dave Robert's coenoflex package for R would 
be a useful alternative but currently is archived on CRAN because of 
some problems in the Fortran code underlying the package.

Rather than have to reinvent the wheel each time I wanted to simulate 
some new data for a paper or to work on a new approach, I decided to 
start my own R package to contain a range of simulators encapsulating 
different response models, numbers of gradients, etc.

At the moment, coenocliner is limited in what it can do practically. 
There is a single response model, the Gaussian response, which is a 
symmetric model of the parameters; the optimum, tolerance and height 
of the response curve. Count data can be generated from this model 
from either a Poisson or negative binomial distribution, using the 
parameterised Gaussian response as the expectation or mean of the 
distribution.

## Installation

No binary packages are currently available for coenocliner. If you 
have the correct development tools you can compile the package 
yourself after downloading the source code from github. Once I work 
out how to link git with svn I'll start a project on 
[R-forge](http://r-forge.r-project.org) which will host binary 
packages of coenocliner.

If you use Hadley Wickham's **devtools** package then you 
can install ggvegan directly from github using functions that 
devtools provides. To do this, install **devtools** from CRAN via

    install.packages("devtools")

then run

    require("devtools")
    install_github("coenocliner", "gavinsimpson")