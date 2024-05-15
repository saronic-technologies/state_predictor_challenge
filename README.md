# Saronic State Prediction Challenge

## Context

Vehicle dynamics on a robot in the water can be challenging. This challenge is a first pass on understanding the challenges behind how vehicle controls in varying sea states can be difficult. 

## Goal

We want two predictors:

- Predict the next vehicle state given a sequence of vehicle
  controls and the current vehicle state.
  - vehicle state is an AHRS message, see the ahrs.log for an example

- Predict the sequence of vehicle controls to achieve a desired vehicle state given a current vehicle state
  - vehicle state is an AHRS message, see the ahrs.log for an example

## Dataset

We have provided two dataset files:
- vehicle_control.csv
  - This is a csv with ts, throttle and turn values
    - ts is a timestamp in UTC
    - throttle is a float value between 0.0-1.0
    - turn is a float value between -1.0 and 1.0
      - 0.0 to 1.0 is a right hand turn
      - -1.0 to 0.0 is a left hand turn

- ahrs.csv  
  - This is a csv with ts, roll_deg, pitch_deg, yaw_deg, ve_mps,
    vn_mps, vu_mps, omega_x_dps, omega_y_dps, omega_z_dps, ax_mps2,
    ay_mps2, az_mps2
    - ts is a timestamp in UTC
    - roll_deg, pitch_deg, and yaw_deg are degrees values
    - ve_mps, vn_mps, and vu_mps are velocities in meters per second in the ENU frame
    - omega_x_dps, omega_y_dps, and omega_z_dps are angular rates in the FRD frame
    - ax_mps2, ay_mps2, and az_mps2 are meter per second^2 accelerations in FRD frame

## Submission

- Send us a git repo with code for the two predictors and instructions on how to run it   
- Also add a README/document with a description explaining the design for your predictor
- Any visualizations or plots to accompany your code are encouraged in your document that explains your design

