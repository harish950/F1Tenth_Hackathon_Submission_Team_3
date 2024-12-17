# F1Tenth_Hackathon_Submission_Team_3

<video width="600" controls>
  <source src="rviz.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Background
Our solution uses a wall following algorithm to navigate around a closed loop track. The goal was to maintain a consistent and safe distance from the wall while ensuring smooth cornering and optimal speeds. 

The grading criteria was the fastest lap time (50%) and number of consecutive laps (50%) within 10 minutes. To maximise our scores, we optimised our algorithm to achieve the maximum number of consecutive laps (with no collisons) albeit each lap being slighlty slower. 

### Algorithm Overview

#### Sensor Input
The algorithm utilizes data from the vehicle’s LaserScan (LIDAR) sensor and odometry to measure distances to obstacles and the walls

#### Control Strategy:
The algorithm uses the Proportional-Integral-Derivative (PID) Controller to maintain the desired distance from the wall. 


#### Dynamic Speed Control:
Adjusts speed dynamically based on the car’s steering angle:
- Faster on straight sections
- Slower on sharp turns to ensure stability

#### Detection of Straights:
Analyzes LaserScan data to detect straight paths by calculating the variance of distances within a certain angular range

#### Output:
- Steering angle: Adjusts the car’s direction to stay near the desired wall.
- Speed: Dynamically scaled to maximize efficiency on straights while maintaining control in turns.


### Results

The following are the results tested usingthe [F1 Tenth Evaluation](https://github.com/NTU-Autonomous-Racing-Team/F1Tenth_Hackathon_Evaluation/tree/main) repo

- 11 consecutive laps (no collisons)
- fastest lap of 51.9 seconds
