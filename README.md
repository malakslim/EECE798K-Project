# EECE798K-Project
Data-Driven Modeling of 5-Dof KUKA youBot Robotic Manipulator

## Abstract

## Dataset
The dataset can be found in the folder "Data". It contains two subfolders, "Data in CSV form" used with FCNN, LSTM, and SINDy models, and "Data_with_estimated_trqs_CSV_form" used with the Hybrid model. 

Within each folder, there are 12 CSV files, each corresponding to a distinct trajectory.

Each CSV file contain a set of columns, each representing a variable, whose value is recorded at all time steps, provided across the rows. The columns that we used include the five joints positions, velocities, and torques. Note that there are additional columns that we did not use. 

In the folder "Data_with_estimated_trqs_CSV_form", five more columns are presented in each CSV file. These columns correspond to the estimated torques of the five joints using Kinematics Dynamics Library (KDL) based on the KUKA youBot URDF file, which were used with the Hybrid model.

## Training and Testing the models

## Results
Predicted and true torque of the five joints across the four models on the first test trajectory:

<img src="https://github.com/malakslim/EECE798K-Project/blob/main/test_traj1_all_models.png" style="width: 50%;">


Predicted and true torque of the five joints across the four models on the second test trajectory:

<img src="https://github.com/malakslim/EECE798K-Project/blob/main/test_traj2_all_models.png" style="width: 50%;">


MSE obtained after filtering the data across the four models:

<img src="https://github.com/malakslim/EECE798K-Project/blob/main/MSE_after_filtering.png" style="width: 50%;">



