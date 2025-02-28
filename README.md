# Quick Guide

<h4>Apply Neural Network to Custom Scheduling Problems</h4>

Create schedules with our neural network for custom offline job scheduling problems on unrelated machines with the [Main.ipynb](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Notebooks/Action_Pointer.ipynb) notebook.

<br><hr>

# Theory

For a detailed explanation of our approach, see our paper that is currently under submission and will be uploaded upon acceptance.

<ins>Probem:</ins><br>

We treat offline job scheduling problems on unrelated machines with an initial occupation and deterministic processing times. Both, jobs and machines, have deadlines and weights for exceeding those deadlines. The goal is to minimize a complex objective function consisting of the total sum of the makespan and the weighted tardiness of jobs and machines.<br>

<ins>Approach:</ins><br>
Our approach is to use deep learning to create efficient schedules. We introduce a novel, sophisticated neural network architecture leveraging different architectures from Natural Language Processing. We thereby handle the inherent flexibility demands induced by varying numbers of jobs, machines and feature dimenions. The problem environment is embedded into a markovian environment: whenever a machine becomes available to either have a pending job assigned or to be terminally deactivated, a state is generated. The state's data is then fed to the neural network which produces a feasible action recommendation. To enable high-precision decision making and fast adaption to different future scenarios, we use supervised training on problem instances with no more than 8 jobs and 4 machines.

<ins>Results:</ins><br>

Our neural network creates almost perfect schedules for small problem instances and demonstrates remarkable generalization capabilities to scheduling problems with much higher numbers of jobs and machines than it was trained on. When comparing induced scheduling costs, our neural network vastly outperforms a competetive advanced dispatching rule.<br>


# Code

All the code is written in Python 3 and uploaded as Jupyter [Notebooks](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/tree/main/Notebooks). The main notebook to apply our approach is [Main.ipynb](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Notebooks/Action_Pointer.ipynb), while the [Full_Framework.ipynb](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Notebooks/Full_Framework.ipynb) notebook explains the entire process of our framework. Details of the neural network architecture are given in the notebook [Neural_Network.ipynb](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Notebooks/Neural_Network.ipynb).

# Files

Besides the directory of notebooks, there are two more directories containing files:

- [Neural Networks](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/tree/main/Neural_Networks): Contains the <i>h5</i>-file of the principal [Neural Network](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Neural_Networks/Neural_Network.h5) after it has underwent full supervised training.
- [Data](https://github.com/Dieguinho1612/Deep-Learning-for-Unrelated-Machines-Scheduling/tree/main/Data): Contains all the data we computed to train, validate and test the neural network.

