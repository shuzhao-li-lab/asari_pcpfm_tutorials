# Tutorials for metabolomics data processing using asari tools

This currently covers asari and the PCPFM pipeline, namely LC-MS data processing, QC, annotation including MS/MS and reporting. Continued development will include more types of data. The URL of this repo is https://github.com/shuzhao-li-lab/asari_pcpfm_tutorials.

Multiple tutorials are linked here:
- [Asari in 5 minutes](/5minutes.md) if you are in a hurry.
- Tutorial for [the web app](/webapp.md).
- [One-hour to understand and master asari and pipeline](/1hour.md).

Planned tutorials (to come):
- Everything you want to know about asari suite.
- Working like a data scientist on Jupyter.

If you are in a class, multiple versions of PowerPoint slides are included in this repo.

If you need install software and/or download data, [this page](/Installation_Preparation.md) may be useful.

Beyond the tutorials, a few example notebooks are provided under [notebooks](/notebooks/) for data analysis.

## Citations of asari suite of tools

- Li, S., Siddiqa, A., Thapa, M., Chi, Y. and Zheng, S., 2023. Trackable and scalable LC-MS metabolomics data processing using asari. Nature Communications, 14(1), p.4113. (https://www.nature.com/articles/s41467-023-39889-1)

- Mitchell, J.M., Chi, Y., Thapa, M., Pang, Z., Xia, J. and Li, S., 2024. Common data models to streamline metabolomics processing and annotation, and implementation in a Python pipeline. PLOS Computational Biology, 20(6), p.e1011912. (https://doi.org/10.1371/journal.pcbi.1011912)

- Li, S. and Zheng, S., 2023. Generalized tree structure to annotate untargeted metabolomics and stable isotope tracing data. Analytical chemistry, 95(15), pp.6212-6217. (https://pubs.acs.org/doi/10.1021/acs.analchem.2c05810) (the khipu paper).

- Mitchell JM, Chi Y, Zheng S, Thapa M, Wang E, Li S. Annotation of Metabolites in Stable Isotope Tracing Untargeted Metabolomics via Khipu-web. Under review. 

The asari suite includes 
- asari (Source code: https://github.com/shuzhao-li/asari, Package Repository: https://pypi.org/project/asari-metabolomics/)
- metDataModel: data models for metabolomics (https://github.com/shuzhao-li-lab/metDataModel)
- mass2chem: common utilities in interpreting mass spectrometry data, annotation (https://github.com/shuzhao-li-lab/mass2chem)
- khipu: a Python library for generalized, low-level annotation of MS metabolomics (https://github.com/shuzhao-li-lab/khipu)
- JMS: Json's Metabolite Services. Search functions, annotation and metabolic models (https://github.com/shuzhao-li-lab/JMS)
- pcpfm pipeline (https://github.com/shuzhao-li-lab/PythonCentricPipelineForMetabolomics)
- asari-x: the eXposome miner (to be released)
