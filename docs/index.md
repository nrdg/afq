# Overview

<!--
## TODO: Expectations for autofq site?
Is autofq the central information repository or is it an overview and visitors should go to individual project websites/github pages?

## TODO: What is AFQ?
Could leverage some content from [AFQ wiki](https://github.com/yeatmanlab/AFQ/wiki)

## TODO: Who is AFQ? 
Background information on project(s)? Who to contact for questions? Citations for usage?

## TODO: Why is AFQ? 
More on motivation. Define intended audiences (e.g., researchers/library users and developers)
-->

<!--
## TODO: What are some intended uses and use cases? 
* Incorporate links to samples/examples/tutorials. 
* What knowledge is assumed? (e.g., neuroanatomy, neuroinformatics, neuro imaging, tractometry, git, python, AWS). 
* Do want to get into providing background resources (e.g., review papers, dictionary terminology)
* Create use case documentation (how to install and run [local vs cloud] vs how to set up development environment and contribute)
-->

This website documents the AFQ projects:
<!--
## TODO: Based on my use case, how do I know which project to use? How do the projects relate/integrate? What are they capable of what are limitations? release schedule information? 
## TODO: What is processing pipeline? diagram? what are steps? which are optional? what are tolerances (recommended settings for use cases)?
## TODO: requirements? assumptions? dependencies? integration? interoperability? standards/specifications?
## TODO: How to diagnose or debug output? tests? confirm validity? sanity checks?
-->

[AFQ-Insight](https://github.com/richford/AFQ-Insight)

[pyAFQ](https://yeatmanlab.github.io/pyAFQ/)
<!-- 
#TODO: Why AFQ and pyAFQ? which should I choose and why?
-->

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