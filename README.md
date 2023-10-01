# Introduction

This repository contains the solution for the image transition test assignments.
1207 input/output image pairs were given with the goal of translating the initial pictures to the target ones by any algorithm of choice.

# Chosen path

At first glance, the difference between inputs and outputs was in blue/orange color mapping of darker/lighter areas.
Comparasence of image/target histograms revealed, that the contrast was decreased (the histogram was "compressed") before color mapping, but clearly not only that.
Since the dataset was sufficiently big, the way of transition was not that obvious and I was not bounded in the sense of algorithm choice, I decided to  train a generative adversarial network (GAN) [pix2pix](https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix). 

# Setup

The model was trained on the local machine since it was more powerful than the virtual machine provided by Google Colaboratory.
Still, the easiest way to check the solution is to look at the [copy at Google Colab]().

Another way is to set the local environment.
For example, on Windows 11 with Python installed:
1. Download or clone the repository 
2. Run command line
3. Run commands:
```
cd "way-to-the-folder-with-a-project"
py -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook
```
4. In the opened Jupyter Notebook interface run the notebook called "model_training.ipynb"

Other details are available in the notebook.

Checkpoints can be downloaded [here](https://drive.google.com/file/d/154-jpEDGW7f0xyUB-r5_FE4alho5svqQ/view?usp=sharing), they should be put in the "training_checkpoints" folder.
