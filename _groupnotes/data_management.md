---
layout: page
title: Data management
---

Scientific data management is a broad term that involves all stages of the digital data lifecycle including capture, analysis, sharing, and preservation. When done well it can help advance science by allowing data to be used and verified more broadly than originally intended.

The extensiveness of what is saved is a strategic decision that needs to balance the costs and benefits to come to a final decision of what to do.

Our typical principle is that the data immediately behind the plots in the scientific manuscript is probably the most useful and likely to be re-used. This is, after all, part of the reason why it was plotted.

## Procedure

1. Ask Mark to generate a [github](https://github.com/) repository. We will generally name these as \<Family name of first author\>\<year\>\<first word of manuscript title\> and save them under Mark's github account [mpmdean](https://github.com/mpmdean).

1. An example of what to do then is provided in [Mazzone2021Antiferromagnetic](https://github.com/mpmdean/Mazzone2021Antiferromagnetic). Please copy the <code>README.rst</code> file from the example to the new repository and update the file to reflect the current manuscript.

1. Commit the data needed to make the plots and sufficient instructions so that
someone with no knowledge of the work could generate the plots.
The easiest way to do this is to use the plotting scripts behind making the plots for the paper. As long the plotting code is reasonably well written it should be adequately clear.

1. A minimum is then to ask Mark to link the repository to [Zenodo](https://zenodo.org/), which is a system designed by CERN to store data and link it to a specific citable item. Each time a release is created in the github repository Zenodo stores the data and creates a new citable item. In most cases, we will just create one release. We suggest this is called First release and named v1.0.0. If, for any reason, an update is needed more releases can be created.

1. A final desirable step is to specify how to run the plotting scripts. We suggest doing this by including a <code>requirements.txt</code> file and using the tool
 [jupyter-repo2docker](https://repo2docker.readthedocs.io/en/latest/). In this way, the code should run by following the instructions in the <code>README.rst</code> file. For most purposes, it will be enough to just copy the <code>requirements.in</code> and <code>requirements.txt</code> files. If more packages are needed, update <code>requirements.in</code> and then run <code>pip-compile requirements.in</code> to generate a new <code>requirements.txt</code> file. This is comprehensively specifying exactly what version python packages are being used and will ensure long-term reproducibility of your code even if future versions of the code include changes that break your code. 
