# EECE798K-Project
Data-Driven Modeling of 5-Dof KUKA youBot Robotic Manipulator

## Abstract
Robotic systems often lack accurate models, especially for complex structures with uncertain dynamics, posing challenges for robust controller design. Data-driven techniques provide a promising solution for this challenge. In this work, we aim to model the inverse dynamics of the 5-DoF KUKA youBot robotic manipulator, needed for implementing inverse dynamics controller. For this purpose, we collected data by maneuvering the robot to perform multiple trajectories, and implemented four different modeling approaches. Fully Connected Neural Networks (FCNNs), Long Short Term Memory (LSTM) networks, and Sparse Identification of Non-linear Dynamical Systems (SINDy), which rely solely on collected data. In addition, we implemented a hybrid model, which takes advantage of the available physical knowledge of robotic systems to enhance the reliability of the estimated dynamics. The four models were then evaluated on a separate dataset. Results show that the hybrid model outperforms the others.
## Dataset
The dataset can be found in the folder "Data". It contains two subfolders, "Data in CSV form" used with FCNN, LSTM, and SINDy models, and "Data_with_estimated_trqs_CSV_form" used with the Hybrid model. 

Within each folder, there are 12 CSV files, each corresponding to a distinct trajectory.

Each CSV file contain a set of columns, each representing a variable, whose value is recorded at all time steps, provided across the rows. The columns that we used include the five joints positions, velocities, and torques. Note that there are additional columns that we did not use. 

In the folder "Data_with_estimated_trqs_CSV_form", five more columns are presented in each CSV file. These columns correspond to the estimated torques of the five joints using Kinematics Dynamics Library (KDL) based on the KUKA youBot URDF file, which were used with the Hybrid model.

## Running the models
The repository contains four notebooks, which were run on Google Colab.
- `FCNN.ipynb` runs the Fully Connected Neural Network (FCNN) model using TensorFlow.
- `LSTM.ipynb` runs the Long Short Term Memory (LSTM) model using TensorFlow.
- `SINDy.ipynb` runs the Sparse Identification of Non-linear Dynamical Systems (SINDy) model using PySINDy.
- `Hybrid.ipynb` runs the Hybrid model, which is based on a FCNN architecture, using TensorFlow.
  
Each notebook provides comprehensive details on data preprocessing, model training, and evaluation specific to its corresponding model.

Please note that you must specify the correct path to the dataset to ensure the proper execution of each notebook.

## Results
Predicted and true torque of the five joints across the four models on the first test trajectory:

<img src="https://github.com/malakslim/EECE798K-Project/blob/main/test_traj1_all_models.png" style="width: 50%;">


Predicted and true torque of the five joints across the four models on the second test trajectory:

<img src="https://github.com/malakslim/EECE798K-Project/blob/main/test_traj2_all_models.png" style="width: 50%;">


MSE obtained after filtering the data across the four models:

<img src="https://github.com/malakslim/EECE798K-Project/blob/main/MSE_after_filtering.png" style="width: 50%;">



