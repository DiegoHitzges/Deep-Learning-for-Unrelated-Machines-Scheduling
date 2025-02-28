# Data

The following directories are data sets of Job Scheduling Problems. The included files are dictionaries. Every item is the data from a state whose amount of remaining Jobs and Machines defines the assigned key. Each directory contained 10.000 instances, only one is kept for illustrative purposes.<br>

The Notebook [LSTM_Data.ipynb](https://github.com/DiegoHitzges/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Notebooks/LSTM_Data.ipynb) has been run on each directory to merge all respective dictionaries. It did so by saving a list of selected data samples belonging to the same key in the sub-directory <i>LSTM_Data_RR</i>. Thereby, the immanent data got transformed into a compatible form to train, validate, test and uptrain our [Neural Network](https://github.com/DiegoHitzges/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Neural_Networks/Neural_Network.h5).<br>

### Data Set 1-10

Used as Training Set.<br>
Created by running [Script_Compute_Data.ipynb](https://github.com/DiegoHitzges/Deep-Learning-for-Unrelated-Machines-Scheduling/blob/main/Notebooks/Script_Compute_Data.ipynb) on a cluster. Random Job Scheduling Problems consisting of 8 Jobs and 4 Machines have been simulated with regards to some chosen conditions. Each of them resulted in a data dictionary, balanced in the distribution of optimality over the feasible actions. Here, the true target values have been computed by brute force. Every directory contains 10.000 such data dictionaries.

### Data Set 98 + 99

Used as Validation and Test set respectively.<br>
Created analogously but without being balanced. Each of them contains 10.000 data dictionaries as well.
