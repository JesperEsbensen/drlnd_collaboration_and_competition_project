# Reacher - robot arm controler

---
Created by Jesper Højmark Esbensen, 2018-11-11.<br>
<br>

This note book will create and train an agent to follow a boble target in the Unity Machine Learning environment Reacher. The solution is based on the general deep reenforcement learning agent supplied in the course [Deep Reinforcement Learning Nanodegree](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893).

<img src="Tennis.png" alt="Tennis Environment" width="500" align="middle"/>

The environment is a robot arm with at spherical target moving around it in a circle. The agent can control the arm with 4 continuous actions. The robot arm gets a reward when the arm touches the sphere. The task is to move the robot arm so it follows the sphere. When a score of more that 30 has been reached, calculated as an average over 100 episods the environment is considdered solved.<br>


### 1. Installation instructions

The robot arm is living in a Unity environment and the agent solving it is a pytorch script run in a Jupyter notebook. Therefore running it will need some setup of tools and environment.

You will need to install python 3.6 and a few packages. One popular way to install python is through Anaconda. A python/R environment. To install this follow the instructions on: https://www.anaconda.com/distribution/.

Create an python environment using the "Create" button and select the python 3.6 version. Start a terminal for the environment and install jupyter.

Install jupyter in the environment. 

    python -m pip install --upgrade pip
    python -m pip install jupyter
   
or reference jupyters home page if you have problems: http://jupyter.org/install

The agent is bulid using Facebook's pyTorch. To install run the followin commands.

    conda install pytorch -c pytorch 
    pip3 install torchvision
    
or reference pyTorch's home page if you have problems: https://pytorch.org/

The environment is build on Unitys ML-agents modul. To run these you will need TensorFlow:

    pip install tensorflow==1.7.1

or reference TensorFlow's home page if you have problems: https://www.tensorflow.org/

Then install the ML-agenst from Unity.
Clone the repository: git clone https://github.com/Unity-Technologies/ml-agents.git
find and change to the directory: ml-agents/python and install the ml-agenst with:

    pip install .

or reference this page if you have problems: https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation-Windows.md


### 2. Clone the "Reacher agent" project

To download this repository and run the reacher agent on your machine clone this github repository with the following command:

    git clone https://github.com/JesperEsbensen/drlnd-continuous-control.git

when cloned unpack the Reacher_Windows_x86_64/Reacher_Windows_x86_64_20Agents in the same location so you get a subfolder: Reacher_Windows_x86_64. If you unpack the environment in a different location you will need to change the path to the environment in the notebook accordingly.

### 3. Train the agent

When you have installed all above packages and cloned the repository to your machine you can open and run the jupyter notebook Report.ipynb. Open the notebook with the following command.

    jupyter notebook
    
Browse to the notebook and open it.

