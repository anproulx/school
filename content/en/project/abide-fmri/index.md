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
I am a Master's student in Psychology currently enrolled at the University of Montreal. My career objective is to work on research projects aiming to discover new ways of characterizing the brain in its pathological states. At the moment, I am working with Sébastien Jacquemont and Pierre Bellec, and the focus of our research is investigating the effect of genetic mutations on fonctional and structural brain phenotypes. More precisely, I have been working with resting-state functional connectivity measures in carrier populations.

By joining the Brainhack School, I hoped to strengthen my computational skills and my knowledge of the applications of machine learning (more specifically to the field of neuroimaging). Not only did I get to work on a cool project, but I also learned about useful tools such as Github. More importantly, I also met a community of brilliant/aware researchers and got to collaborate with other students across the world!

#### Mikkel

## Project background

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
For the purpose of this project, we used the preprocessed open source database ABIDE (see Preprocessed Connectomes Project), available through Nilearn. This data contains structural, functional and phenotypic data of 539 individuals with autism and 573 typical controls.

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
The first part of this project consisted of exploring different ways that we could organize our project as a team. We decided that our project's structure would consist of three parts: 1) a python script for standardized data preparation, 2) machine learning and 3) presentation. 

The python script served to prepare the fMRI data for the machine learning in a standardized way. Each of the team members used that python script to then branch of in different Jupyter notebooks and implement different models and cross-validation techniques.


### Tools I learned during this project

 * **Meta-project** P Bellec learned how to do a meta project for the first time, which is developping a framework while using it at the same time. It felt really weird, but somehow quite fun as well.
 * **Github workflow-** The project allowed us to learn about Github's .
 * **Project content** Through the project reports generated using the template, it is possible to learn about what exactly the brainhack school students are working on.

### Results

#### Deliverable 1: report template

You are currently reading the report template! I will let you judge whether it is useful or not. If you think there is something that could be improved, please do not hesitate to open an issue [here](https://github.com/brainhack-school2020/project_template/issues) and let us know.

#### Deliverable 2: project gallery

There is not yet a project gallery, as BHS 2020 is the first edition that will incorporate it on the website. You can still check out the [2019 BHS github organization](https://github.com/mtl-brainhack-school-2019)

##### ECG pupilometry pipeline by Marce Kauffmann

The repository of this project can be found [here](https://github.com/mtl-brainhack-school-2019/ecg_pupillometry_pipeline_kaufmann). The objective was to create a processing pipeline for ECG and pupillometry data. The motivation behind this task is that Marcel's lab (MIST Lab @ Polytechnique Montreal) was conducting a Human-Robot-Interaction user study. The repo features:
 * a [video introduction](http://www.youtube.com/watch/8ZVCNeX42_A) to the project.
 * a presentation [made in a jupyter notebook](https://github.com/mtl-brainhack-school-2019/ecg_pupillometry_pipeline_kaufmann/blob/master/BrainHackPresentation.ipynb) on the results of the project.
 * Notebooks for all analyses.
 * Detailed requirements files, making it easy for others to replicate the environment of the notebook.
 * An overview of the results in the markdown document.

##### Other projects
Here are other good examples of repositories:
- [Learning to manipulate biosignals with python](https://github.com/mtl-brainhack-school-2019/franclespinas-biosignals) by François Lespinasse
- [Run multivariate anaylysis to relate behavioral and electropyhysiological data](https://github.com/mtl-brainhack-school-2019/PLS_PV_Behaviour)
- [PET pipeline automation and structural MRI exploration](https://github.com/mtl-brainhack-school-2019/rwickens-sMRI-PET) by Rebekah Wickens
- [Working with PSG [EEG] data from Parkinson's patients](https://github.com/mtl-brainhack-school-2019/Soraya-sleep-data-in-PD-patients) by Cryomatrix
- [Exploring Brain Functional Activation in Adolescents Who Attempted Suicide](https://github.com/mtl-brainhack-school-2019/Anthony-Gifuni-repo) by Anthony Gifuni

#### Deliverable 3: Instructions
 

## Conclusion and acknowledgement

