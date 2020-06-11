---
type: "project" # DON'T TOUCH THIS ! :)
date: "2020-05-16" # Date you first upload your project.
# Title of your project (we like creative title)
title: "How accuratly can we predict autism from fMRI data?"

# List the names of the collaborators within the [ ]. If alone, simple put your name within []
names: [Emily Chen, Andréanne Proulx, Mikkel Schöttner]

# Your project GitHub repository URL
github_repo: https://github.com/brainhack-school2020/abide-fmri

# If you are working on a project that has website, indicate the full url including "https://" below or leave it empty.
website:

# List +- 4 keywords that best describe your project within []. Note that the project summary also involves a number of key words. Those are listed on top of the [github repository](https://github.com/brainhack-school2020/project_template), click `manage topics`.
# Please only lowercase letters
tags: [machine learning, fMRI, autism, open science]

# Summarize your project in < ~75 words. This description will appear at the top of your page and on the list page with other projects..

summary: "In this project, we set out to compare different classfication algorithms and cross-validation methods to see how well each one was able to predict autism diagnosis from the resting-state fMRI data in the ABIDE dataset."

# If you want to add a cover image (listpage and image in the right), add it to your directory and indicate the name
# below with the extension.
image: "project_abideteam.png"
---
<!-- This is an html comment and this won't appear in the rendered page. You are now editing the "content" area, the core of your description. Everything that you can do in markdown is allowed below. We added a couple of comments to guide your through documenting your progress. -->

## Project definition

### Background

#### Emily 

Hello! I am an (incoming) fourth year undergraduate student at McGill University studying computer science and urban health geography with a minor in cognitive science. I am a research assistant with Isabelle Arseneau-Bruneau in the Zatorre Lab and have been learning a lot about neuroscience research while (hopefully) lending some of my technical skills to Isabelle's PhD work exploring the effect of musical training on FFR. 

When joining the BrainHack School, I was looking forward in particular to working on a project at the intersection of neuroscience and CS because my previous classes rarely focused on the application of the abstract concepts we learned. Upon completion of the BrainHack School, I had the opportunity to learn from and collaborate with talented neuroscience researchers and participants, write a machine learning script using python and neuroscience data, and gain hands-on practice in reproducibility efforts and good project management. 

You can find me on GitHub at [emilyemchen](https://github.com/emilyemchen) and on Twitter at [@emilyemchen](https://twitter.com/emilyemchen).

#### Andréanne
Hi! I am a student in Cognitive Neuroscience recently enrolled in a Master's in Psychology at the University of Montreal. My career objective is to work on research projects aiming to discover new ways of characterizing the brain in its pathological states. At the moment, I am working with Sébastien Jacquemont and Pierre Bellec, and the focus of our research is investigating the effect of genetic mutations on fonctional and structural brain phenotypes. More precisely, I have been working with resting-state functional connectivity measures in carrier populations.

By joining the Brainhack School, I hoped to strengthen my computational skills and my knowledge in the applications of machine learning (more specifically to the field of neuroimaging). Not only did I get to work machine learning project, but I also got to learn about useful tools such as Github. More importantly, I also met a community of brilliant/aware researchers and got to collaborate with other students across the world!

#### Mikkel

#### Project background

Several studies have found functional connectivity profil in the default mode network in people with ASD (Anderson, 2014). Based on these findings, rs-fMRI data have been used to predict autism by training a classifier on the multi-site ABIDE data set (Nielsen et al., 2013). This project aims to replicate these findings.


### Tools

This project will rely on the following tools:
 - Jupyter Notebook
 - Python libraries: Scikit-learn, Nilearn, Seaborn, Matplotlib, Pyplot
 - Git
 - Github
 - Venv
 - Docker
 
### Data
For the purpose of this project, we used the preprocessed open source database ABIDE (see Preprocessed Connectomes Project), available through Nilearn. This data contains structural, functional and phenotypic data of 539 individuals with autism and 573 typical controls. We will be using the preprocessed fMRI data as well as the information regarding diagnosis.

### Deliverables

At the end of this project, we will have:
 - A python script 
 - 3 Jupyter Notebooks, each containing the code for different cross-validation methods
 - Requirement.txt file
 - README file
 
Presentation:
 - Jupyter Notebook (presentation.ipynb)
 
Visualizations: 
 - Links to Plotly visualization
 
## Results

### Progress overview
The first part of this project consisted of exploring different ways in which we could organize our project as a team. We decided that our project's structure would consist of three parts: 1) standardized data preparation, 2) machine learning and 3) presentation. 

We wrote a python script which served to prepare the fMRI data for the machine learning in a standardized way. Each of the team members branched off in different Jupyter Notebooks, where they ran that python script to prepare the data. Then, we  implemented different models and cross-validation techniques which are describe in further detail below. 


### Tools we learned during this project

 * **Python librairies** Nilearn, Matplotlib, Plotly, Sklearn (dimensionality reduction, test-train split, gridsearch, cross-validation methods, evaluate performance)
 * **Github workflow-** Push, pull, fork, merge, pull requests, issues, etc. Also learned team management and organization.
 * **Venv** Make requirement.txt file
 * **Git**  Track files such as Jupyter Notebook
 * **Machine learning** Concepts & tools for applications of machine learning to the neuroimaging field 

### Results

#### Deliverable 1: Jupyter notebooks

##### Leave-site-out cross-validation

[*`leave-site-out-cv_classifier.ipynb`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/leave-site-out-cv_classifier.ipynb)

This notebook contains code to run a linear support vector classification to predict autism from resting state data. It uses leave-group-out cross-validation using site as the group variable. The results give a good estimate of how stable the model is. While for most of the sites the prediction works above chance level, for some, autism is predicted only at or even below chance level.

##### K-fold and leave-one-out cross-validation
[*`kfold_LeaveOneOut_cv_classifier.ipynb`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/kfold_LeaveOneOut_cv_classifier.ipynb)

This notebook contains the code to run support vector classification, k neirest neighbors, decision tree and random forest on the Abide dataset. The models are trained and evaluated using k-fold and leave-one out cross-validation methods. We obtain accuracy scores that represent how skilled the model is at predicting the labels of unseen data.  Leave-ont out cross validation gives more accurate predictions than kfold cross validation. The accuracy values range from 55.8% to 69.2%.

#####

#### Deliverable 2: [*`prepare_data.py`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/prepare_data.py)

This script

* downloads the data
* extracts the time series of 64 regions of interest defined by the BASC brain atlas
* computes the correlations between time series for each participant
* uses a principal component analysis for dimensionality reduction



#### Deliverable 3: Visualization
* [Emily's GitHub Repository](https://github.com/emilyemchen/bhs2020-dataviz)
* [Andréanne's GitHub Repository](https://github.com/brainhack-school2020/anproulx-fMRI-autism)
* [Mikkel's GitHub Repository](https://github.com/brainhack-school2020/mschoettner_fMRI-ML), [link to the plot](https://mschoettner.github.io/brainhack_visualization/)

#### Deliverable 4: Presentation

[presentation](https://github.com/brainhack-school2020/abide-fmri/tree/master/presentation)


## Conclusion and acknowledgement
A special thank you to all the 2020 BrainHack School organizers for making this event an amazing and eye opening learning experience!

 - Pierre Bellec (Mentor)
 - Désirée Lussier-Lévesque (Mentor)
 - Alexa Pichet-Binette (Mentor)
 - Sebastian Urchs (Mentor)
 - Jean-Baptiste Poline
 - Tristan Glatard
 - Benjamin de Leener
 - Elizabeth DuPre
 - Ross Markello
 - Peer Herholz
 - Samuel Guay
 - Valerie Hayot-Sasson
 - Karim Jerbi
 - Greg Kiar
 - Jake Vogel
 - Agâh Karakuzu
 
## References

1. Choosing appropriate estimators with scikit-learn https://scikit-learn.org/stable/tutorial/machine_learning_map/
2. Benchmarking functional connectome-based predictive models for resting-state fMRI (for classification estimator inspiration) https://hal.inria.fr/hal-01824205
3. Getting the data using nilearn fetch https://nilearn.github.io/modules/generated/nilearn.datasets.fetch_abide_pcp.html
4. Python Data Science Handbook GitHub and website https://github.com/jakevdp/PythonDataScienceHandbook

Anderson, J. S., Patel, V. B., Preedy, V. R., & Martin, C. R. (2014). Cortical underconnectivity hypothesis in autism: evidence from functional connectivity MRI. Comprehensive guide to autism, 1457, 1471.

Nielsen, J. A., Zielinski, B. A., Fletcher, P. T., Alexander, A. L., Lange, N., Bigler, E. D., ... & Anderson, J. S. (2013). Multisite functional connectivity MRI classification of autism: ABIDE results. Frontiers in human neuroscience, 7, 599.

