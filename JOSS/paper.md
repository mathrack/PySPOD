---
title: 'PySPOD: A Python package for Spectral Proper Orthogonal Decomposition (SPOD)'
tags:
  - Python
  - dynamical systems
  - nonlinear dynamics
  - data-driven dynamics
  - data mining
authors:
  - name: Mengaldo G.
    orcid: 0000-0002-0157-5477
    affiliation: "1, 2" # (Multiple affiliations must be quoted)
  - name: Author Without ORCID
    affiliation: 2
  - name: Author with no affiliation
    affiliation: 3
affiliations:
 - name: National University of Singapore
   index: 1
date: 2 November 2020
bibliography: paper.bib

# Optional fields if submitting to a AAS journal too, see this blog post:
# https://blog.joss.theoj.org/2018/12/a-new-collaboration-with-aas-publishing
<!-- aas-doi: 10.3847/xxxxx <- update this with the DOI from AAS once you know it.
aas-journal: Astrophysical Journal <- The name of the AAS journal. -->
---

# Summary

Large unstructured datasets may contain complex coherent patterns that 
evolve in time and space, and that the human eye cannot grasp. These 
patterns are frequently essential to unlock our understanding of complex 
systems that can arise in nature, such as the evolution of the atmosphere 
in the short (weather prediction) and long term (climate prediction), 
the behavior of turbulent flows, and the dynamics of plate tectonics, 
among several others. Identifying these coherent structures can therefore 
prove crucial to facilitate the construction of modeling tools that can 
help anticipate scenarios that would otherwise be not predictable

Within this context, dynamical system theory, complemented with recent 
advances in machine learning and data mining tools, is achieving tremendous 
advances in our ability to acquire actionable information from data arising 
from complex systems. Singular-value decomposition based tools, in particular, 
are a promising area that is gaining popularity, due to its links to 
reduced order modeling and dynamical systems. Also, these tools can be used 
in the context of machine learning as additional inputs to the architecture, 
thereby enhancing the datasets and possibly helping in the interpretability 
of the results. 

While, several variants of singular-value decomposition based techniques 
have been proposed in the literature, this library provides an efficient 
implementaiton of the so-called spectral proper orthogonal decomposition 
(SPOD) [@lumley1970], [@towne2017], that is also referred to as spectral 
empricial orthogonal function (SEOF) in the weather and climate community 
[@schmidt2019a].


# Statement of need

`PySPOD` is a modular Python package that implements three different variants 
of SPOD, (i) a low storage, (ii) a low RAM, and (iii) a streaming version 
[@schmidt2019b]. The three versions differ in terms of I/O and RAM requirements. 
The low storage version allows faster computations, and it is intended for small 
datasets, or large RAM machines. The low RAM and streaming versions can handle 
large datasets, but they are typically slower than the low storage counterpart. 
The API to the library offers a flexible and user-friendly experience, and 
the library can be complemented with additional SPOD algorithms in an easy-to-implement
way. The structure of the library and the use of Python enable efficient 
interfacing with low level and highly optimized libraries (written in C 
or Fortran) for the calculation of e.g. the fast Fourier transform, eigenvalue 
decomposition, and other linear algebra operations. Users can also take advantage 
of the ready-to-use postprocessing tools offered, and they can easily extend 
the postprocessing functionalities to suit their needs. 

`PySPOD` is designed to be used in different fields of engineering and applied 
science, including weather and climate, fluidmechanics, seismology, among others.
It can be used as a production code, for the analysis of large datasets, as well 
as for experimenting on smaller problems. Users can be students and experts alike.


# Mathematics

Single dollars ($) are required for inline mathematics e.g. $f(x) = e^{\pi/x}$

Double dollars make self-standing equations:

$$\Theta(x) = \left\{\begin{array}{l}
0\textrm{ if } x < 0\cr
1\textrm{ else}
\end{array}\right.$$

You can also use plain \LaTeX for equations
\begin{equation}\label{eq:fourier}
\hat f(\omega) = \int_{-\infty}^{\infty} f(x) e^{i\omega x} dx
\end{equation}
and refer to \autoref{eq:fourier} from text.

# Citations

Citations to entries in paper.bib should be in
[rMarkdown](http://rmarkdown.rstudio.com/authoring_bibliographies_and_citations.html)
format.

If you want to cite a software repository URL (e.g. something on GitHub without a preferred
citation) then you can do it with the example BibTeX entry below for @fidgit.

For a quick reference, the following citation commands can be used:
- `@author:2001`  ->  "Author et al. (2001)"
- `[@author:2001]` -> "(Author et al., 2001)"
- `[@author1:2001; @author2:2001]` -> "(Author1 et al., 2001; Author2 et al., 2002)"

# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

# Acknowledgements

We acknowledge contributions from Brigitta Sipocz, Syrtis Major, and Semyeong
Oh, and support from Kathryn Johnston during the genesis of this project.

# References
