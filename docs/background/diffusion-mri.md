# Resources for learning the basics of diffusion MRI

## Here are some readings to introduce the field

**A great overview of the field:**

> Wandell BA (2016) Clarifying Human White Matter. Annu Rev Neurosci 39(1):annurev-neuro-070815-013815.

**Review paper on fiber tractography methods:**

> Jeurissen B, Descoteaux M, Mori S, Leemans A (2019) Diffusion MRI fiber tractography of the brain. NMR Biomed 32(4):1–22.

**Two papers from our group focused on using diffusion MRI to study brain development and plasticity:**

> Huber E, Donnelly PM, Rokem A, Yeatman JD (2018) Rapid and widespread white matter plasticity during an intensive reading intervention. Nat Commun 9(1):2260.

> Huber E, Henriques RN, Owen JP, Rokem A, Yeatman JD (2019) Applying microstructural models to understand the role of white matter in cognitive development. Dev Cogn Neurosci 36(February):100624.

**There are so many tractography algorithms. Which one is the best?**
There is no simple answer to this question: it depends on your goals, the data acquisition as well as the subjects being studied. For example, many of the cutting-edge algorithms depend on collecting many diffusion directions across multiple b-values and this often isn't feasible in clinical studies or pediatric studies. Understanding the tradeoffs between different algorithms is important. Recent work by Girard and colleagues [@girard2020cortical] compared the compendium of tractography algorithms implemented in mrtrix and DIPY to "gold-standard" tracer studies done in rhesus macaque monkey. This recent paper provides a thoughtful description of how to think about gold standards and how to evaluate the tradeoffs between different algorithms. They conclude that many tractography algorithms are quite good in terms of sensitivity/specificity and provide useful guidance in distinguishing between different algorithms.

> Girard, Gabriel, Roberto Caminiti, Alexandra Battaglia-Mayer, Etienne St-Onge, Karen S. Ambrosen, Simon F. Eskildsen, Kristine Krug, et al. 2020. “On the Cortical Connectivity in the Macaque Brain: A Comparison of Diffusion Tractography and Histological Tracing Data.” NeuroImage 221 (July): 117201.

## TRACTOMETRY - Automated Fiber Quantification (AFQ)

Tractometry refers to methods for analzying properties of the brain's major white matter connections. Automated Fiber Quantification (AFQ) is a tractometry toolbox we developed for analyzing white matter tracts in individuals and groups. There is a MATLAB and a Python version of AFQ.

**Here is the paper that introducued the method:**

    Yeatman JD, Dougherty RF, Myall NJ, Wandell BA, Feldman HMM (2012) Tract profiles of white matter properties: automating fiber-tract quantification. PLoS One 7(11):e49790.

And here is a more recent paper introducing a browser-based visualization and analysis tool to support reproducibility and data sharing

> Yeatman JD, Richie-Halford A, Smith JK, Keshavan A, Rokem A (2018) A browser-based tool for visualization and analysis of diffusion MRI data. Nat Commun 9(1):940.

## Blogs and tutorials

The OHBM has a blog with videos based on the educational course given at the
annual meeting [here](https://www.ohbmbrainmappingblog.com/blog/ohbm-ondemand-how-to-diffusion-mri).

Here is a tutorial walking through the basics of diffusion MRI
https://www.imagilys.com/diffusion-tensor-imaging-dti/

# Software tutorials to learn how to analyze diffusion MRI data

## AFQ (MATLAB)

The original matlab version of AFQ comes with tutorials and example data.

1) Clone the AFQ repo (and dependencies listed in README.txt) here: https://github.com/yeatmanlab/AFQ
2) Read the brief wiki page: https://github.com/yeatmanlab/AFQ/wiki
3) In a MATLAB terminal type `help AFQ_run` and then run the example here to process the example dataset. The example data is included in the repo and the tutorial should run without any additional configuration.
4) See the AFQ_example totorial as well https://github.com/yeatmanlab/AFQ/blob/master/tutorials/AFQ_example.m
5) See the Group Comparison example https://github.com/yeatmanlab/AFQ/blob/master/tutorials/AFQ_example_GroupComparison.m

## pyAFQ

All new development is occuring on pyAFQ which leveraged the [Diffusion Imaging in Python (DIPY)](https://dipy.org/) package to provide a much more flexible and extensible version of AFQ. DIPY also has an incredible [gallery of tutorials](https://dipy.org/tutorials/) covering everything from fitting diffusion models to voxels, tractography, microstructural models and more! To get going with pyAFQ:
1) Check out the [pyAFQ GitHub page](https://yeatmanlab.github.io/pyAFQ/)
2) This documents how to
   * [Install pyAFQ](https://yeatmanlab.github.io/pyAFQ/installation_guide.html) which can be done easliy with `pip install AFQ` (including all dependencies)
   * [The basics of organizing data and running pyAFQ](https://yeatmanlab.github.io/pyAFQ/usage.html)
   * [A series of examples as Jupyter Notebooks](https://yeatmanlab.github.io/pyAFQ/auto_examples/index.html). These notebooks will automatically pull the necesary data from public repos so you don't need to do anything beyond installing pyAFQ
   * [The API is also documenter here](https://yeatmanlab.github.io/pyAFQ/autoapi/index.html)



Public Datasets with diffusion MRI data are described in our [datasets page](datasets.md)
