# state_predictor_challenge

## Goal

We want two predictors:

- Given a sequence of vehicle controls and the
  current state of the vehicle output the next state of the vehicle

- Given a current state and a desired state what is the sequence of
  vehicle controls we need to achieve the desired state

## Dataset

We have provided two dataset files:
- vehicle_control.log
  - This is a csv with ts, throttle and turn values
    - ts is a timestamp in UTC
    - throttle is a float value between 0.0-1.0
    - turn is a float value between -1.0 and 1.0
      - 0.0 to 1.0 is a right hand turn
      - -1.0 to 0.0 is a left hand turn

- ahrs.log
  - This is a csv with ts, roll_deg, pitch_deg, yaw_deg, ve_mps,
    vn_mps, vu_mps, omega_x_dps, omega_y_dps, omega_z_dps, ax_mps2,
    ay_mps2, az_mps2
    - ts is a timestamp in UTC
    - roll_deg, pitch_deg, and yaw_deg are degrees values
    - ve_mps, vn_mps, and vu_mps are velocities in meters per second in the ENU frame
    - omega_x_dps, omega_y_dps, and omega_z_dps are angular rates in the FRD frame
    - ax_mps2, ay_mps2, and az_mps2 are meter per second^2 accelerations in FRD frame