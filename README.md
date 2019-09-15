# tumor-tensors

## Abstract *: Summarize everything in a few sentences.* 
We built a system to convert annotated nii files into pixel contours, then fill those contours and render them into grids or mp4s. 

## Introduction *: What's the problem? Why should we solve it?*
We wanted to render both the MRI dicoms and make an augmented display of contours around labeled tumors to visually inspect how predictive models are performing. 

## Methods *: How did we go about solving it?*
We used pydom and matplot lib for rendering. We also developed some utility methods for loading nii data, converting nii labels into per-dicom/slice contours, used matplotlib and shapely to augment the dicom display, and used ffmpeg to convert plots images into an mp4 video.

## Results *: What did we observe? Figures are great!*
![example segmentations](https://i.ibb.co/cLgkhgG/example-contours.png)

## Conclusion/Discussion: 

### Please make sure you address ALL of the following:

#### *1. What additional data would you like to have*
It would have been nice to have more attribute data about segmented tumors (texture, density, etc). It also would have been nice to already have nii data in a per-dicom data structure.

#### *2. What are the next rational steps?* 
Integrate these rendering tools into predictive model pipelines.

#### *3. What additional tools or pipelines will be needed for those steps?*
No extra tools are needed for rendering, it can function stand-alone.

#### *4. What skills would additional collaborators ideally have?*
Computer vision.

## Reproduction: *How to reproduce the findings!*
Open docker or run our Jupyter notebooks.

### Docker

*The Docker image contains <R/jupyter> notebooks of all analyses and the dependencies to run them. *Be sure to note if you need any special credentials to access data for these analyses, **don't package restricted data** in your containers!*

Instructions for running the following notebooks: *be sure to adjust these instructions as necessary! check out https://github.com/Sage-Bionetworks/nf-hackathon-2019 for example containers and instructions*

1. `docker pull <your dockerhub repo>/<this container>` command to pull the image from the DockerHub
2. `docker run <your dockerhub repo>/<this container>` Run the docker image from the master shell script

### Important Resources *: primary data, github repository, Synapse project, dockerfile link etc.*


