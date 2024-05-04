# EECE798K-Project
Data-Driven Modeling of 5-Dof KUKA youBot Robotic Manipulator

## Abstract

## Dataset
The dataset can be found in the folder "Data". It contains two folders, "Data in CSV form" used with FCNN, LSTM, and SINDy models, and "Data_with_estimated_trqs_CSV_form" used with the Hybrid model. Each folder contains 12 CSV files, each corresponding to one trajectory. The CSV files contain a set of columns, each representing a variable, whose value is given at each row, corresponding to a different time step. The columns that we used include the five joints positions, velocities, and torques. Note that there are additional columns that we did not use. In the folder "Data_with_estimated_trqs_CSV_form", 5 more additional columns are presented and used for training the hybrid model, which correspond to the estimated torques using Kinematics Dynamics Library (KDL) based on the KUKA youBot URDF file.

## Training and Testing the models

## Results
