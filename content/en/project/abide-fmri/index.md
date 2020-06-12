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

summary: "Is autism associated with a distinct neurofunctional signature? If so, how accuratly are we able to predict the diagnosis based on fMRI data. In this project, we set out to compare different classfication algorithms and cross-validation methods to see how well each one was able to predict autism diagnosis from the resting-state fMRI data in the ABIDE dataset."

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
Hi! I am an incoming master's student in Psychology at the University of Montreal. My background is in cognitive neuroscience and my career objective is to work on research projects aiming to discover new ways of characterizing the brain in its pathological states. At the moment, I am working with Sébastien Jacquemont and Pierre Bellec, and the focus of our research is in investigating the effect of genetic mutations on fonctional and structural brain phenotypes. More precisely, I have been working with resting-state functional connectivity measures in carrier populations with developmental disorders.

By joining the Brainhack School, I hoped to strengthen my computational skills and my knowledge in the applications of machine learning  to the field of neuroimaging. Not only did I get to work on a machine learning problem specific to my field, but I also got to learn about useful tools such as Github. More importantly, I also met a community of brilliant/aware researchers and got to collaborate with other students, even across the world!

#### Mikkel

#### Project background

Several studies have found functional connectivity profil in the default mode network in people with ASD (Anderson, 2014). Based on these findings, rs-fMRI data have been used to predict autism by training a classifier on the multi-site ABIDE data set (Nielsen et al., 2013). This project's scientific aim is to replicate these findings.

### Becoming a Team 
The three of us joined forces when we realized that we shared many similar learning goals and interests. With such similar project ideas, we figured we would accomplish more working together by each taking on a different cross-validation methods to train various machine learning models. 


### Team Project Management

We all shared a common interest in making our project as reproducible as possible. This goal meant creating a transparent, collaborative workflow that could be tracked at any time by anyone. To achieve this objective, we utilized the many features that GitHub has to offer, all of which you can see in action at our shared repository [here](https://github.com/brainhack-school2020/abide-fmri).
* **Branches:** used to simultaneously on our own parts and then push changes to the master branch
* **Pull requests:** created when making changes to the master branch
* **Issues:** used to communicate with each other and keep track of tasks
* **Tags:** used to keep issues organized
* **Milestones:** used to keep our main goals in mind (Week 4 presentation and final deliverable)
* **Projects:** used to track various aspects of our work 

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
 - Links to Plotly visualizations
 
## Results

### Progress overview
The first part of this project consisted of exploring different ways in which we could organize our project as a team. We decided that our project's structure would consist of three main elements: 1) standardized data preparation, 2) machine learning 3) containerization of the working environment. 

We wrote a python script to standardize the fMRI data preparation before the machine learning. Each of the team members branched off in different Jupyter Notebooks, where they ran that python script to prepare the functional data from the ABIDE dataset. Then, we  implemented different models and cross-validation techniques which are describe in further detail below. 


### Tools we learned during this project

 * **Python librairies:** Nilearn, Matplotlib, Plotly, Sklearn (dimensionality reduction, test-train split, gridsearch, cross-validation methods, evaluate performance)
 * **Github workflow:** Push, pull, fork, merge, pull requests, issues, etc. Also learned team management and organization.
 * **Venv:** Make requirement.txt file
 * **Git:**  Track files such as Jupyter Notebook
 * **Machine learning:** Concepts & tools for applications of machine learning to the neuroimaging field 

### Results

#### Deliverable 1: Jupyter notebooks

##### Leave-site-out cross-validation

[*`leave-site-out-cv_classifier.ipynb`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/leave-site-out-cv_classifier.ipynb)

This notebook contains code to run a linear support vector classification to predict autism from resting state data. It uses leave-group-out cross-validation using site as the group variable. The results give a good estimate of how stable the model is. While for most of the sites the prediction works above chance level, for some, autism is predicted only at or even below chance level.

##### K-fold and leave-one-out cross-validation
[*`kfold_leave_one_out_cv_classifier.ipynb`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/kfold-leave-one-out-cv_classifier.ipynb)

This notebook contains the code to run support vector classification, k neirest neighbors, decision tree and random forest on the Abide dataset. The models are trained and evaluated using k-fold and leave-one out cross-validation methods. We obtain accuracy scores that represent how skilled the model is at predicting the labels of unseen data.  Leave-ont out cross validation gives more accurate predictions than kfold cross validation. The accuracy values range from 55.8% to 69.2%.

##### Group k-folds cross-validation

[*`group-kfolds-cv_classifier.ipynb`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/group-kfolds-cv_classifier.ipynb)

![Results cross-validation methods](result_cv.png)

#### Deliverable 2: [*`prepare_data.py`*](https://github.com/brainhack-school2020/abide-fmri/blob/master/code/prepare_data.py)

This script

* downloads the data
* extracts the time series of 64 regions of interest defined by the BASC brain atlas
* computes the correlations between time series for each participant
* uses a principal component analysis for dimensionality reduction

To fetch and prepare the data set you can call the `prepare_data.py` script like this:

`./prepare_data.py data_dir output_dir`

or alternatively:

`python prepare_data.py data_dir output_dir`

where
* `data_dir` is the directory where you want to save the data or have it already saved and
* `output_dir` is the directory where you want to store the outputs the script generates.

The notebooks also call the `prepare_data` function from the preparation script.

#### Deliverable 3: Visualizations
* [Emily's GitHub Repository](https://github.com/emilyemchen/bhs2020-dataviz)
* [Andréanne's GitHub Repository](https://github.com/brainhack-school2020/anproulx-fMRI-autism)
* [Mikkel's GitHub Repository](https://github.com/brainhack-school2020/mschoettner_fMRI-ML), [link to the plot](https://mschoettner.github.io/brainhack_visualization/)

#### Deliverable 4: Presentation

The presentation slides can be viewed [here](https://www.canva.com/design/DAD-ByEQaXI/QLgHbYgnKd-xDWJXVnaGDA/view) on Canva, which is the platform we used to create the slides. A video of our presentation can be viewed on this project page. We presented our work to the BrainHack School on June 5, 2020 using the RISE integration in a Jupyter notebook, which can be found [here](https://github.com/brainhack-school2020/abide-fmri/tree/master/presentation). 

#### Deliverable 5: Documentation
 [`README.md`](https://github.com/brainhack-school2020/abide-fmri/blob/master/README.md) 
 
 [`requirements.txt`](https://github.com/brainhack-school2020/abide-fmri/blob/master/requirements.txt) 

This file increases reproducibility by helping to ensure that the scripts run correctly on any machine. To make sure that all scripts work correctly, you can create a virtual environment using pythons built-in library `venv`. To do this, follow these steps:

1. Clone repo and navigate to folder in a shell
2. Create a virtual environment in a folder of your choice: `python -m venv /path/to/folder`
3. Activate it (bash command, see [here](https://docs.python.org/3/library/venv.html) how to activate in different shells): `source /path/to/folder/bin/activate`
4. Install all necessary requirements from requirements file: `pip install -r requirements.txt`
5. Create kernel for jupyter notebooks: `ipython kernel install --user --name=abide-ml`
6. Open a jupyter notebook: `jupyter-notebook`, then click the notebook you want to run
7. Select different kernel by clicking *Kernel -> Change Kernel -> abide-ml*
8. Run the code!
 
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

**Scientific articles**: 

Anderson, J. S., Patel, V. B., Preedy, V. R., & Martin, C. R. (2014). Cortical underconnectivity hypothesis in autism: evidence from functional connectivity MRI. Comprehensive guide to autism, 1457, 1471.

Nielsen, J. A., Zielinski, B. A., Fletcher, P. T., Alexander, A. L., Lange, N., Bigler, E. D., ... & Anderson, J. S. (2013). Multisite functional connectivity MRI classification of autism: ABIDE results. Frontiers in human neuroscience, 7, 599.
