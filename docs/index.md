# Overview

This website documents the AFQ projects:

[AFQ-Insight](https://github.com/richford/AFQ-Insight)

[pyAFQ](https://yeatmanlab.github.io/pyAFQ/)

[AFQ-Browser](https://yeatmanlab.github.io/AFQ-Browser/)


## Aims of these projects

Human brain white matter contains the long-range connections between different
brain regions. Diffusion MRI (dMRI) is a powerful imaging technology that
provides non-invasive *in vivo* measurements of these connections. These
measurements have provided compelling evidence that the biophysical properties
of these connections account for individual variation in many important
cognitive skills, and they predict clinical symptoms across a variety of
psychiatric and neurological disorders (reviewed in [@Rokem2017JoVWM] and [@wandell2016clarifying]).

One of the major challenges in analyzing dMRI data is that the details of the 3D
structure of white matter anatomy varies between individuals. *Tractometry* is a
methodology that solves this problem by identifying specific connections in each
individual's brain, using known anatomical structures as the coordinate system
to compare measurements across subjects. We are implementing open-source
software for tractometry and to extract the biophysical properties of major
brain connections. Based on this tractometry framework, we are also implementing
novel methods for statistical learning and visualization of the features of
white matter anatomy that lead to individual differences in the behavioral
measurements. We will facilitate further exploration of these results and their
integration with other datasets through web-based visualization tools. Taken
together these projects provide a comprehensive
**data science toolbox for end-to-end analysis of dMRI data**: the delineation
of trajectories of white matter tracts within individual brains, integration of
measurements across individuals, inferences about the role of connections in
individual variability of their cognitive abilities and behavior, and
exploration of the results through interactive visualizations. This is
particularly important as the research community is developing large datasets.



\bibliography