# CSE 5280 — Robot Arm Interference in Crowd Evacuation

Nick Speranza

This project extends multi-agent evacuation simulation by introducing a robotic manipulator whose end-effector acts as a dynamic obstacle during crowd evacuation.

Particles move through the environment using gradient-based optimization on a shared objective containing:

* goal attraction
* wall avoidance
* obstacle repulsion
* social interaction terms
* dynamic avoidance of robot interference

The robot continuously observes evacuation flow near exits, detects emerging particle clusters, predicts their short-term motion, and moves its end-effector using inverse kinematics to interfere with the dominant escape stream.

No explicit path planning is used for either the crowd or the robot.
The crowd reacts naturally through force interactions, while the robot closes the loop through perception, prediction, and control.

## 📄 View Report (Recommended)

Open the fully rendered notebook:

https://nbviewer.org/github/nicolas-speranza/robotic-interference-with-crowd-evacuation-nicolas-speranza/blob/main/robotic_interference_with_crowd_evacuation.ipynb

## Contents

* Mathematical formulation
* Crowd simulation environment
* Exit-focused clustering
* Motion prediction of evacuation streams
* Robot inverse kinematics control
* Dynamic obstacle interaction
* Quantitative experiments
* Trajectory visualizations
* Animation and video export
* Discussion and conclusions

## Experiments Compared

* baseline crowd evacuation without robot
* robot interference with cluster tracking
* prediction-based interception
* sensitivity to dynamic crowd re-routing

## Key Result

A closed-loop interaction emerges between crowd motion and robot control: the robot identifies dominant evacuation streams, predicts future cluster motion, and strategically places its end-effector to interfere with evacuation, causing rerouting and local congestion without explicit coordination.

## Repository Files

* `cse5280_robot_arm_interference_corrected_final.ipynb` — full notebook with experiments, analysis, and animation
* `README.md` — project overview and report link
* `robot_interference.mp4` *(optional)* — short simulation video
