# Hybrid Rigid-Body and Learning-Based Dynamics Modeling for a Flexible 2-DoF Robotic Arm

This repository contains the notebook and processed dataset used for the project **Hybrid Rigid-Body and Learning-Based Dynamics Modeling for a Flexible 2-DoF Robotic Arm**.

The project compares three torque-prediction approaches for a flexible-link robotic arm using the MERIt/TUDOR dataset:

1. **Ridge Regression Model**  
   A black-box baseline that predicts joint torque from joint position, velocity, and acceleration.

2. **Physics-Based Rigid-Body Dynamics Model**  
   A white-box model that evaluates the rigid-body dynamics equations using parameters computed from published robot specifications.

3. **Physics-Based Regression Model**  
   A gray-box model that preserves the rigid-body dynamics structure but identifies the grouped dynamic parameters directly from data using least-squares regression.

For each model, a Gaussian Mixture Regression residual model is trained to estimate the remaining torque error. This residual correction is used to improve torque prediction in the presence of flexible-link dynamics, compliance, vibration, friction mismatch, and other unmodeled effects.

## Repository Structure

```text
.
├── README.md
├── requirements.txt
├── 618Data_Final.ipynb
└── data
    └── MERIt_0Payload_data.xlsx