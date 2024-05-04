# EECE798K-Project
Data-Driven Modeling of 5-Dof KUKA youBot Robotic Manipulator

## Abstract

## Dataset
The dataset can be found in the folder "Data". It contains two subfolders, "Data in CSV form" used with FCNN, LSTM, and SINDy models, and "Data_with_estimated_trqs_CSV_form" used with the Hybrid model. 

Within each folder, there are 12 CSV files, each corresponding to a distinct trajectory.

The CSV files contain a set of columns, each representing a variable, whose value is recorder at all time steps, provided across the rows. The columns that we used include the five joints positions, velocities, and torques. Note that there are additional columns that we did not use. 

In the folder "Data_with_estimated_trqs_CSV_form", five more columns are presented and used for training the hybrid model, which correspond to the estimated torques using Kinematics Dynamics Library (KDL) based on the KUKA youBot URDF file.

## Training and Testing the models

## Results
