3-part Tutorial on Self Supervised Denoising
=========

This repository contains the codes created for the Self-supervised denoising tutorial presented at Transform 2022.

Authors: 
 - Claire Birnie (claire.birnie@kaust.edu.sa), and 
 - Sixiu Liu (sixiu.liu@kaust.edu.sa)
 
The tutorial was originally presented as a live-stream event on YouTube on April 27 2022 at 11 UTC. 

YouTube Link: https://www.youtube.com/watch?v=d9yv90-JCZ0

Tutorial overview
---------------------------

Self-supervised learning offers a solution to the common limitation of the lack of noisy-clean pairs of data for training deep learning seismic 
denoising procedures.

In this tutorial, we will explain the theory behind blind-spot networks and how these can be used in a self-supervised manner, removing any 
requirement of clean-noisy training data pairs. We will deep dive into how the original methodologies for random noise can be adapted to handle 
realistic noise in seismic data, both pseudo-random noise and structured noise. Furthermore, each sub-topic presented will be followed by a live, 
code-along session such that all participants will be able to recreate the work shown and can afterwards apply it to their own use cases. 

If you found the tutorial useful please consider citing our work in your studies:

> Birnie, C., M. Ravasi, S. Liu, and T. Alkhalifah, 2021, The potential of self-supervised networks for random noise 
> suppression in seismic data: Artificial Intelligence in Geosciences.

> Liu, S., C. Birnie, and T. Alkhalifah, 2022, Coherent noise suppression via a self-supervised deep learning scheme: 
> 83rd EAGE Conference and Exhibition 2022, European Association of Geoscientists & Engineers, 1–5

Repository overview
---------------------------

The top level of the repository contains the skeleton tutorial notebooks that will be completed during the live YouTube tutorial.
This level also contains the necessary files for setting up the conda environment (and submitting jobs for those working on the 
KAUST IBEX cluster). As well as the standard git files - README, .gitignore, etc. 

The **Solutions** folder contains the completed notebooks. Note, there is no one *correct* way in which to write the necessary functions 
therefore the proposed solutions are only there to serve as guidance. 

Disclaimer: the code has all been written and tested on Linux operating systems, where GPU access is available. Neither of the authors are professional 
software developers therefore, whilst we have spent significant time testing the code, we cannot gaurantee it is free of bugs.

Installation instructions
---------------------------

As these procedures are based on deep-learning we encourage you to use a GPU if possible.

**Data Download**

The data utilised in this tutorial series can be downloaded from: 
https://kaust-my.sharepoint.com/:u:/g/personal/birniece_kaust_edu_sa/ETavD6gzmutAsrVbfv84BVcBlS0tONM2CyGfMr6YjLrSvA?e=8gXGLD

This folder contains synthetically generated shot gathers modelled using the Hess VTI model and a post-stack seismic section
of the Hess VTI model. The folder also contains a field data example originally downloaded from Madagascar of a post-stack
seismic section that is often used benchmarking new random noise suppression algorithms.


**Environment creation**

We have made a conda environment file which contains all the necessary packages to run the tutorials. For ease of use,
an installation script has been written to create the conda environment and  check the necessary packages were 
correctly installed. The environment can be created with the following command (executed when in this folder):

    ./install_env.sh
    
The enviornment can then be activated by running the command:

    conda activate ssd_tutorial
    



